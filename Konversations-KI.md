# Architecture & Model Stack: Episodic Multi-User VR Voice Agent

**Hardware Target:** Apple Silicon (Mac Studio M3 Ultra, 512 GB Unified Memory)
**Frameworks:** Apple MLX, FastAPI, Unity (NativeWebSocket)

---

## 0. Problem Statement / Sprint Epic: Episodic Multi-User AI Voice Assistant in VR

### 1. Initial Situation
An interactive Virtual Reality (VR) environment built in Unity requires an integrated, highly responsive AI assistant. The AI runs locally on high-performance hardware and must interact seamlessly with both the users and the dynamic environment.

### 2. Core Challenges & Requirements

#### A. Multimodal Real-Time Processing (Audio & JSON)
The AI must participate in a continuous conversation without significant latency. It must process native live audio inputs while simultaneously understanding asynchronous, non-verbal data updates (e.g., environmental or machine states formatted as JSON) sent from the Unity environment. 

#### B. Multi-Speaker Attribution & Audio Multiplexing
At least two human participants are active in the VR space. They use separate microphones, meaning the audio is hardware-separated by channel. The AI must accurately distinguish between the users, attribute statements to the correct person, and maintain social conversational context while filtering out cross-talk.

#### C. Episodic Memory & State Management (The Rolling 5-Minute Constraint)
To maintain low latency and prevent KV-cache bloat, conversation sessions are segmented. 
* **Overlapping Reset:** To avoid latency spikes, a background summarization process begins before the current round completely ends.
* **State Summarization:** A secondary text model generates a concise, accurate state summary of the finishing round in the background.
* **Next Round Initialization:** The subsequent round is initialized seamlessly using this text-based summary and the latest JSON data.
* **Duration:** This episodic state-reset loop will repeat for a total of 4 to 5 consecutive rounds.

### 3. Objective
To engineer a local, low-latency AI architecture bridging a Unity client and a local inference server. The system must orchestrate continuous audio streams, multiplex distinct microphone channels using Voice Activity Detection (VAD), inject real-time JSON data with active preemption capabilities, and manage an episodic state-reset loop using parallel background summarization.

---

## 1. Phase 1: Active Conversation Round (Real-Time Audio + JSON + Multi-User)
For the active phases, a multimodal end-to-end model is required that can process text tokens (JSON data, system states) and audio tokens (user speech) within the same context window without latency.

* **Recommended Model:** `Mistral-Voxtral-24B-Instruct` (MLX-quantized to 8-bit or 4-bit)
* **Alternative:** `GLM-4-Voice-9B` (if extremely low latency and rapid "Real-Time Interruption" are the highest priority).
* **Rationale:** The 24B parameter class fully utilizes the Apple Silicon compute cores while leaving massive headroom in the 512GB RAM for the parallel text model.

### Multi-Speaker Handling & Modality Interleaving
Since two separate audio streams arrive from Unity, they must be processed carefully to avoid disrupting the model's attention mechanisms.
* **Voice Activity Detection (VAD):** A highly lightweight model like `Silero VAD` runs in the middleware (under 2ms latency). It analyzes which channel is active and aggressively blocks background noise/cross-talk from the silent channel.
* **Speaker Embeddings / Safe Interleaving:** If the Voice-LLM supports native speaker embeddings in the audio tensor, this is the preferred method. Otherwise, text tokens (e.g., `[System: User A is speaking]`) are injected during speaker changes with a micro-pause, ensuring the audio stream isn't broken mid-utterance.

---

## 2. Phase 2: Round Transition & State Summarization (Text-Only)
Instead of a hard stop at 5 minutes, an overlapping transition is used to prevent memory bandwidth bottlenecks and "dead time" in the VR environment.

* **Recommended Model:** `Meta-Llama-3-70B-Instruct` (MLX-quantized to 4-bit)
* **Rationale:** The 70B model guarantees the highest precision in extracting facts and preventing hallucinations in subsequent rounds. It is held in RAM parallel to the 24B model.
* **Rolling Summaries:** At the 4-minute mark, the background STT (Speech-to-Text) transcript of the first 4 minutes is passed to Llama-3 to begin the heavy summarization task. Only the final minute is processed dynamically at the transition point.
* **Strict STT-VAD Alignment:** The background STT model strictly adheres to the Silero VAD timestamps to prevent corrupt transcripts caused by audio bleed between the VR users.

---

## 3. Infrastructure & Middleware Stack

To bridge the Unity client and the local inference backend, the following stack is implemented:

* **Inference Backend:** `mlx-lm` and Hugging Face `speech-to-speech` repository (optimized for Metal Performance Shaders).
* **Server / Routing:** `FastAPI` (Python).
    * Opens an asynchronous WebSocket.
    * Integrates `Silero VAD` for channel analysis (User A vs. User B).
    * Routes active PCM audio chunks to the Voice-LLM.
    * **Active Preemption Logic:** Monitors incoming JSON strings. If a critical state is detected (e.g., `{"status": "critical"}`), FastAPI instantly sends a `StopGeneration` command to MLX, aborting the AI's current audio output to allow immediate processing and reaction to the new data.
* **Unity Client:** `NativeWebSocket` (or comparable C# library).
    * Captures VR headset microphones separately (Channel A and Channel B) and streams raw bytes.
    * Receives audio bytes from the server and pushes them into a dynamic `AudioSource` for Spatial Audio in the VR room.
    * Pushes JSON updates to the server whenever scene/machine data changes.

---

## 4. Schematic Prompt Flow & State Management (Overlapping Approach)

### Start Round 1
**System Prompt (Voice-LLM):** `You are an AI assistant in a VR environment. You help two users analyze real-time data. Be concise and precise.`
`[JSON_INJECT: {"machine": "X-1", "status": "nominal", "temperature": 45}]`
`[System: User A is speaking:]` *(...Audio stream from Mic A starts...)*
`[System: User B is speaking:]` *(...Audio stream from Mic B starts...)*

### Critical Interrupt Event (e.g., Minute 2)
1. Unity sends `[JSON_INJECT: {"machine": "X-1", "status": "critical", "temperature": 85}]`.
2. FastAPI intercepts, halts current Voice-LLM generation via `MLX interrupt`.
3. Model immediately parses the new JSON and generates a contextual verbal warning.

### Transition Phase (Minute 4 to Minute 5)
1. WebSocket flags `INITIATE_ROLLING_SUMMARY`.
2. Background STT transcript (Min 0-4) is sent to **Llama-3 70B** to generate a pre-computation of the state.
3. At Minute 5, the final 60 seconds of transcript are appended, Llama-3 finalizes the `STATE_INJECT` rapidly.
4. Voice-LLM KV-Cache is cleared via MLX `clear_cache()`.

### Start Round 2 (Seamless)
**System Prompt (Voice-LLM):** `You are an AI assistant...`
`[STATE_INJECT (generated by Llama 70B): In the previous round, User A and User B identified a critical temperature spike in machine X-1. They are currently looking for the optimal coolant.]`
`[JSON_INJECT: {"machine": "X-1", "status": "cooling", "temperature": 60, "valves_open": true}]`
`[System: User B is speaking:]` *(...Audio stream from Mic B starts...)*