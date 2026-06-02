# Architektur & Modell-Stack: Episodischer Multi-User VR-Voice-Agent

**Hardware-Zielumgebung:** Apple Silicon (Mac Studio M3 Ultra, 512 GB Unified Memory)
**Frameworks:** Apple MLX, FastAPI, Unity (NativeWebSocket)

---

## 0. Problem Statement / Sprint Epic: Episodic Multi-User AI Voice Assistant in VR

### 1. Initial Situation
An interactive Virtual Reality (VR) environment built in Unity requires an integrated, highly responsive AI assistant. The AI runs locally on high-performance hardware (Apple Silicon, 512GB Unified Memory) and must interact seamlessly with both the users and the dynamic environment.

### 2. Core Challenges & Requirements

#### A. Multimodal Real-Time Processing (Audio & JSON)
The AI must participate in a continuous conversation without significant latency. It must process native live audio inputs while simultaneously understanding asynchronous, non-verbal data updates (e.g., environmental or machine states formatted as JSON) sent from the Unity environment. 

#### B. Multi-Speaker Attribution
At least two human participants are active in the VR space. They use separate microphones, meaning the audio is hardware-separated by channel. The AI must be able to accurately distinguish between the users, attribute statements to the correct person, and maintain social conversational context.

#### C. Episodic Memory & Context Management (The 5-Minute Constraint)
To maintain low latency and prevent KV-cache bloat, a single continuous conversation session is strictly limited to a maximum of 5 minutes. 
* **Hard Reset:** After 5 minutes, the audio stream and the AI's context window must be completely flushed.
* **State Summarization:** The system must generate a concise, accurate text summary of the finished round in the background.
* **Next Round Initialization:** The subsequent round must be initialized seamlessly using only this text-based summary and the latest JSON data.
* **Duration:** This episodic state-reset loop will repeat for a total of 4 to 5 consecutive rounds.

### 3. Objective
To engineer a local, low-latency AI architecture bridging a Unity client and a local inference server. The system must successfully orchestrate continuous audio streams, multiplex distinct microphone channels using Voice Activity Detection (VAD), inject real-time JSON data into the inference context, and manage an episodic state-reset loop using parallel background summarization.

---

## 1. Phase 1: Aktive Gesprächsrunde (Echtzeit Audio + JSON + Multi-User)
Für die 5-minütigen aktiven Phasen wird ein multimodales End-to-End-Modell benötigt, das Text-Tokens (JSON-Daten, Sprecher-IDs) und Audio-Tokens (Nutzer-Sprache) im selben Kontextfenster latenzfrei verarbeiten kann.

* **Empfohlenes Modell:** `Mistral-Voxtral-24B-Instruct` (MLX-quantisiert auf 8-bit oder 4-bit)
* **Alternative:** `GLM-4-Voice-9B` (falls extrem niedrige Latenz und schnelle "Real-Time Interruption" priorisiert werden).
* **Begründung:** Die 24B-Parameter-Klasse lastet den M3 Ultra gut aus, lässt aber noch massiv Platz im RAM für das parallele Text-Modell. Das Modell versteht eingespeiste JSON-Updates in Millisekunden und kann nativ darauf Bezug nehmen.

### Multi-Speaker Handling (Multiplexing)
Da zwei getrennte Audioströme aus Unity ankommen, dürfen diese nicht gemischt werden.
* **Voice Activity Detection (VAD):** Ein extrem leichtgewichtiges Modell wie `Silero VAD` läuft in der Middleware. Es analysiert in unter 2ms, welcher Kanal gerade aktiv ist, und blockt das Rauschen des stillen Kanals ab.
* **Text-Interleaving:** Wechselt der Sprecher, pausiert der Stream für eine Millisekunde, injiziert ein Text-Token (z. B. `[System: User A is speaking]`) und schiebt dann die Audio-Daten dieses Kanals hinterher.

---

## 2. Phase 2: Runden-Reset & State-Zusammenfassung (Text-Only)
Nach 5 Minuten wird der Kontext geleert. Ein zweites, reines Text-Modell übernimmt im Hintergrund das sprechergetrennte Transkript der letzten Runde und konsolidiert es zu einer dichten Zusammenfassung.

* **Empfohlenes Modell:** `Meta-Llama-3-70B-Instruct` (MLX-quantisiert auf 4-bit)
* **Begründung:** Mit 512 GB RAM kann das 70B-Modell problemlos *parallel* zum Voxtral-24B-Modell im Speicher gehalten werden. Es garantiert höchste Präzision beim Extrahieren von Fakten und verhindert Halluzinationen in Folgerunden.
* **Transkriptions-Pflicht:** Das kleine STT-Hilfsmodell (Speech-to-Text), das im Hintergrund mitläuft, muss die VAD-Daten zwingend nutzen, um ein sauberes Skript im Format `User A: ... \n User B: ...` an Llama-3 zu übergeben.

---

## 3. Infrastruktur & Middleware-Stack

Um die Brücke zwischen Unity und dem lokalen Mac Studio zu schlagen, empfiehlt sich folgender Stack:

* **Inference Backend:** `mlx-lm` und Hugging Face `speech-to-speech` Repository (optimiert für Metal Performance Shaders / Apple Silicon).
* **Server / Routing:** `FastAPI` (Python).
    * Eröffnet einen asynchronen WebSocket.
    * **Neu:** Integriert `Silero VAD` zur Kanal-Analyse (User A vs. User B).
    * Routet aktive PCM-Audio-Chunks an Voxtral und injiziert bei Sprecherwechseln dynamische Text-Tags in den Stream.
    * Routet eingehende JSON-Strings als Text-Injects in den Voxtral-Kontext.
* **Unity Client:** `NativeWebSocket` (oder vergleichbare C#-Library).
    * Greift die VR-Headset-Mikrofone separat ab (Kanal A und Kanal B) und streamt rohe Bytes.
    * Empfängt Audio-Bytes vom Server und pusht sie in eine dynamische `AudioSource` für Spatial Audio im VR-Raum.
    * Pusht JSON-Updates an den Server, sobald sich die Szene/Maschinendaten ändern.

---

## 4. Schematischer Prompt-Ablauf (State Management)

*(Hinweis: Alle System-Prompts und Injects erfolgen auf Englisch, um die Instruktions-Treue der LLMs zu maximieren.)*

### Start Runde 1
**System Prompt (Voxtral):** `You are an AI assistant in a VR environment. You help two users analyze real-time data. Be concise and precise.`
`[JSON_INJECT: {"machine": "X-1", "status": "critical", "temperature": 85}]`
`[System: User A is speaking:]` *(...Audio-Stream von Mikrofon A startet...)*
`[System: User B is speaking:]` *(...Audio-Stream von Mikrofon B startet...)*

### Ende Runde 1 (Nach 5 Min)
1. WebSocket sendet `END_ROUND`.
2. Audio-Streams stoppen.
3. Das strukturierte Transkript (inkl. Speaker-Tags) wird an **Llama-3 70B** gesendet, um einen kompakten State zu generieren.
4. Voxtral KV-Cache wird via MLX `clear_cache()` komplett geleert.

### Start Runde 2
**System Prompt (Voxtral):** `You are an AI assistant...`
`[STATE_INJECT (generated by Llama 70B): In the previous round, User A and User B decided to manually cool down machine X-1. They are currently looking for the optimal coolant.]`
`[JSON_INJECT: {"machine": "X-1", "status": "cooling", "temperature": 60, "valves_open": true}]`
`[System: User B is speaking:]` *(...Audio-Stream von Mikrofon B startet...)*