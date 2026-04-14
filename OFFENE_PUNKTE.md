# Offene Punkte: VR in KMU – Forschungs- und Transferprojekt

> Stand: März 2026
> Zweck: Sukzessive Abarbeitung zur Vorbereitung des Zwischenberichts
> Status-Legende: `[ ]` offen · `[~]` in Bearbeitung · `[x]` erledigt

---

## Neu · Dokumentstruktur (Buch/ Ordner)

> **[x] Erledigt (März 2026)**: Neue Markdown-basierte Dokumentstruktur unter `Buch/` erstellt. Alle LaTeX-Inhalte wurden portiert. Quarto + Typst-kompatibel.

### Struktur des finalen Dokuments (`Buch/`)

```
Buch/
├── _quarto.yml                          ← Quarto-Konfiguration (Typst + HTML)
├── index.md                             ← Vorwort (TODO: verfassen)
├── 01_einfuehrung.md                    ← aus Einführung.tex
├── 02_framework.md                      ← Framework-Übersicht, 7 Domänen, SVG-Referenz
├── 03_betriebswirtschaftlicher_nutzen.md ← Domäne 1 + Kosten-Nutzen + Beispiele-Template
├── 04_anwendungsszenarien.md            ← Domäne 2 + Meeting-Charakterisierung + Szenarien
├── 05_wissenschaftliche_basis.md        ← Domäne 3 + UTAUT + Spieltheorie-Grundlagen
├── 06_empirische_untersuchung.md        ← Domäne 4 + Workshop-Design + TODOs
├── 07_person_individuum.md              ← Domäne 5 + Für/Gegen-Indikationen + VR-Sickness
├── 08_technische_implementation.md      ← Domäne 6 + aus Detaillierte Beschreibung.tex
├── 09_trends.md                         ← Domäne 7 + aus Zukunftsausblick.tex
├── 10_implementierungsleitfaden.md      ← Assessment + Entscheidungsmatrix + Strategien + Risiken
├── Workshop/
│   ├── workshop_szenario.md             ← Vollständige Workshop-Dokumentation (teilweise TODO)
│   └── spieltheorie.md                  ← aus Game-Theory.tex, vollständig konvertiert
└── Anhang/
    ├── A_glossar.md                     ← 37 Begriffe aus VR Meetings in KMU.md
    ├── B_checklisten.md                 ← aus Branchenspezifische Checklisten.tex
    ├── C_utaut_fragebogen.md            ← Fragebogenstruktur (teilweise TODO)
    └── D_ressourcen.md                  ← Kuratierte Ressourcen und Literatur
```

### Beispiel-Template (pro Kapitel)

Jedes Framework-Domänen-Kapitel enthält eine Vorlage für Beispieleinträge mit diesen Feldern:
- **Typ**: Forschungsprojekt / Pilotprojekt / Marktprodukt
- **Organisation**, **Branche**, **Region**, **Link**
- **Rolle von VR** in diesem Beispiel
- **Relevanz für die Domäne**
- **Beschreibung** + **Erkenntnisse**

> Alle Kapitel enthalten `<!-- TODO -->`-Marker für noch ausstehende Inhalte.

---

## A · Empirische Basis (höchste Priorität)

### A1 · Workshop-Dokumentation (Verhandlungsszenario)
- [x] Beschreibung des Szenarios: Rahmenbedingungen, Aufgabenstellung, VR-Umgebung → `Buch/Workshop/workshop_szenario.md`
- [x] Teilnehmerstruktur dokumentieren (Anzahl, Rollen, demographische Merkmale, VR-Vorerfahrung) → `Buch/06_empirische_untersuchung.md`, Abschnitt „Stichprobe"
- [x] Ablauf und Methodik des Workshops festhalten → `Buch/Workshop/workshop_szenario.md` (Phasen 1–4), `Buch/06_empirische_untersuchung.md` (Messinstrumente)
- [x] Qualitative Beobachtungen und Nutzerrückmeldungen aufbereiten → `Buch/06_empirische_untersuchung.md`, Abschnitt „Qualitative Inhaltsanalyse" (102 codierte Aussagen, 6 Kategorien; Stand April 2026)
- [x] UTAUT-Messdaten (soweit erhoben) aufbereiten und auswerten → `Buch/06_empirische_untersuchung.md`, Abschnitte ATI-S, FMS, UEQ-S (n=15, Stand April 2026)
- [x] CIPD-Variablen: Welche wurden erfasst? Ergebnisse dokumentieren → `Buch/06_empirische_untersuchung.md`, Abschnitt „Verhaltensbeobachtung" (5 Gruppen, Stand April 2026)
- [~] Verbindung zum spieltheoretischen Modell herstellen: Was hat das Modell vorhergesagt, was wurde beobachtet?
  - Spieltheoretische Einordnung des implementierten Designs (nicht des ursprünglichen Cobb-Douglas-Modells) eingefügt in `Buch/Workshop/spieltheorie.md`, Abschnitt „Spieltheoretische Einordnung des implementierten Experiment-Designs" (April 2026)
  - Verknüpfung mit beobachtetem Verhalten (Reputationsaufbau, Cheap-Talk-Muster, bounded rationality) hergestellt
  - Noch ausstehend: quantitativer Vergleich der beobachteten Allokationen mit Gleichgewichtsvorhersagen (erfordert Zugang zum Spiel-Code)

### A2 · Hypothesen formulieren und dokumentieren
- [ ] Die im Framework (PDF S. 19–20) genannten „Hypothesen" als Kernentität sind bislang nirgends explizit aufgelistet – konkreter Hypothesenkatalog fehlt vollständig
- [ ] Hypothesen aus dem Desk Research ableiten und schriftlich fixieren (theoretisch begründet, KMU-spezifisch, falsifizierbar)
- [ ] Zuordnung jeder Hypothese zu einer Framework-Domäne
- [ ] Ergebnis der Verhandlungs-Workshops: Welche Hypothesen wurden bestätigt/falsifiziert?

### A3 · UTAUT-Fragebogen
- [ ] Vollständigen UTAUT-Fragebogen ausarbeiten (passend zu den erhobenen CIPD-Variablen)
- [ ] Im LaTeX-Anhang einbinden (Kapitel „Angepasste Fragebögen zur Erfassung der VR-Bereitschaft" ist aktuell leer)
- [ ] Anpassung an das Verhandlungsszenario prüfen

---

## B · Literatur und Quellenarbeit

### B1 · Vergleichsstudien zu VR-Tests in realen Szenarien
- [x] Recherche: Empirische Studien zu **VR-gestützten Verhandlungen** — abgeschlossen (April 2026)
  - Eingearbeitet in `Buch/04_anwendungsszenarien.md` (Abschnitt „Belegte Fallstudien"):
    - Ding, Brinkman & Neerincx (2020), IJHCS, DOI: 10.1016/j.ijhcs.2020.102400 (peer-reviewed, Q1)
    - Klaue et al. (2020), WI2020, DOI: 10.30844/wi_2020_t3-klaue (Beat the Bot / HNU)
    - Moser et al. (2020), Cyberpsychology, DOI: 10.1089/cyber.2020.0065 (VR vs. Video vs. F2F)
- [x] Recherche: **VR-Rollenspiele und Simulationen** im Unternehmenskontext — abgeschlossen
  - MARLA (TU Berlin, AVRiL Goldpreis 2021): VR-Serious-Game für Offshore-Windenergie-Azubis
  - PALFINGER VR1 (WindEnergy Hamburg 2024): Kranführer-Zertifizierung für Offshore-Wind
  - Deutsche Bahn EVE (DELINA 2020): VR-Zugbegleiter-Training → Verweis in Kap. 03
- [x] Recherche: **Asymmetrische VR-Interaktionen** — abgedeckt durch Beat the Bot (Mensch vs. KI-Avatar) und Microsoft Mesh (VR- vs. Desktop-Teilnehmer, bereits in Kap. 04)
- [ ] Gefundene Studien in `literatur.bib` einpflegen: Ding et al. (2020), Moser et al. (2020), Klaue et al. (2020), Teichmann et al. (2023) — noch ausstehend
  - Zusätzlich prüfen: PwC (2020) als Graue Literatur; Meyer Werft / PALFINGER / DNV als Webquellen
  - Empfehlung: Für Webquellen BibTeX @misc mit url= und urldate= verwenden

### B2 · Quellenprobleme beheben
- [ ] Quelle [6] im PDF (Çolak & Yılmaz, 2022) ist mit „??" markiert – Vollständigkeit und Korrektheit prüfen
- [x] Illustrative Fallstudien in `Buch/04_anwendungsszenarien.md` wurden **explizit als illustrative Szenarien** gekennzeichnet (Hinweis-Box zu Beginn des Abschnitts „Spezifische VR-Szenarien", April 2026)
  - Die fiktiven Firmennamen (TechTool GmbH, HomeConcept AG etc.) stammen aus dem LaTeX-Archiv und wurden nicht in die Markdown-Version übernommen; die bestehenden Kap.-04-Fallstudien (Automobilzulieferer, Elektronikhersteller etc.) sind nun als illustrativ deklariert
- [ ] Regionale Beispiele (Maschinenbauer Flensburg, Tourismusunternehmen Ostsee) in Kap. 04 noch als illustrativ kennzeichnen oder durch echte Belege ersetzen → ggf. aus Testfall-Abdeckung (J) ableiten
- [ ] Abgleich: Quellen im PDF (12 Einträge) vs. Quellen in `literatur.bib` – Lücken schließen, insbesondere: Awa et al. (2015), Elia et al. (2021), Wohlgenannt et al. (2020), Flavián et al. (2019), Radianti et al. (2020)

#### Neue belegte Fälle in `Buch/04_anwendungsszenarien.md` (Stand April 2026)

| Quelle | Typ | Norddeutsch-Bezug | DOI / Link |
|---|---|---|---|
| Ding et al. (2020), IJHCS | Peer-reviewed | Nein | 10.1016/j.ijhcs.2020.102400 |
| Moser et al. (2020), Cyberpsychology | Peer-reviewed | Nein | 10.1089/cyber.2020.0065 |
| Klaue et al. (2020) / Beat the Bot HNU | Konferenzbeitrag | Preis Hamburg | 10.30844/wi_2020_t3-klaue |
| Meyer Werft VR | Unternehmenswebsite | **Ja (Niedersachsen)** | meyerwerft.de |
| PALFINGER VR1 | Pressemitteilung | **Ja (Hamburg)** | palfinger.com |
| MARLA / TU Berlin | Hochschulprojekt | Ja (Offshore SH/NDS) | marla.tech |
| DNV Survey Simulator | Unternehmenswebsite | **Ja (Hamburg)** | dnv.com |
| Deutsche Bahn EVE | Fachpresse | Ja (DE) | → Kap. 03 |
| PwC Soft Skills (2020) | Graue Literatur | Nein | → Kap. 03 |
| Teichmann et al. (2023) / API-KMU | Springer-Buchkapitel | Nein (Brandenburg) | → Kap. 06 |

---

## C · Verbindung der Projektelemente

### C1 · Framework (PDF) ↔ Markdown-Leitfaden
- [x] Das PDF-Framework beschreibt 7 Domänen – die neue `Buch/`-Struktur ist vollständig nach diesen 7 Domänen gegliedert (Kap. 03–09)
- [x] Entscheidung gefallen: Framework als `Buch/02_framework.md` ist ein eigenes Kapitel mit SVG-Einbettung
- [x] Querverweise im Leitfaden sind durch die Kapitelstruktur implizit gegeben
- [ ] Framework_v2.drawio.svg in `Buch/02_framework.md` prüfen: Pfad `../Framework_v2.drawio.svg` korrekt?

### C2 · VR Meetings in KMU.md ↔ PDF-Framework
- [x] Inhalte aus VR Meetings in KMU.md (Glossar 37 Begriffe, Meeting-Charakterisierung) wurden in `Buch/` integriert
- [ ] Meeting-Typ-Tabellen (Kollaboration, Schulung, Produktentwicklung, Marketing, Fernwartung) noch vollständig in `Buch/04_anwendungsszenarien.md` einpflegen
- [x] Entscheidung: `Buch/02_framework.md` ist die offizielle Frameworkbeschreibung

### C3 · Game-Theory.tex integrieren
- [x] Game-Theory.tex wurde vollständig nach `Buch/Workshop/spieltheorie.md` konvertiert
- [x] Entscheidung: Workshop-Anhang (`Buch/Workshop/`) mit Verlinkung aus `Buch/05_wissenschaftliche_basis.md` und `Buch/06_empirische_untersuchung.md`
- [ ] Verbindung Modell → Workshop-Design → Ergebnisse noch inhaltlich ausarbeiten (→ A1)

---

## D · Inhaltliche Lücken im LaTeX-Leitfaden

### D1 · Leere / unfertige Kapitel (Status im neuen Buch/ Ordner)
- [ ] **Vorwort** (`Buch/index.md`): noch leer – verfassen
- [~] **Fragebogen** (`Buch/Anhang/C_utaut_fragebogen.md`): Struktur angelegt, Items noch auszuarbeiten (→ A3)
- [x] **Glossar** (`Buch/Anhang/A_glossar.md`): 37 Begriffe aus `VR Meetings in KMU.md` übertragen
- [~] **Ressourcen** (`Buch/Anhang/D_ressourcen.md`): Grundstruktur mit Journals, Plattformen, Förderangeboten angelegt – vertiefen
- [x] **Hinweis Software-Tool**: In `Buch/` nicht übernommen (unklar ob Tool existiert; → G)

### D2 · Technische Inkonsistenz: Checklisten-Datei
- [x] Checklisten-Inhalt vollständig in `Buch/Anhang/B_checklisten.md` eingebunden (LaTeX-Problem nicht relevant im neuen MD-Workflow)

---

## E · Technische Fehler im LaTeX-Projekt

> **Hinweis**: Das neue `Buch/`-Projekt ist Markdown-basiert (Quarto + Typst). Die folgenden LaTeX-Probleme sind für den neuen Workflow nicht mehr relevant. Das LaTeX-Projekt (`main.tex` etc.) bleibt als Archiv erhalten.

- [x] **Framework_v2.drawio.svg** ist jetzt in `Buch/02_framework.md` eingebunden (relativer Pfad `../Framework_v2.drawio.svg`)
- [ ] **Fehlende Abbildungen**: Grafiken (`vr_success_factors_by_industry.png` etc.) existieren nicht – im neuen Markdown-Workflow durch Beschreibungstext ersetzt; Grafiken bei Bedarf noch erstellen/beschaffen
- [ ] **Bibliographie**: `Buch/_quarto.yml` referenziert `../literatur.bib` – Einträge in `literatur.bib` prüfen und ggf. ergänzen (→ B2)

---

## F · Zwischenbericht für das Förderprojekt

- [ ] **Klären**: Welches Format und welchen Umfang verlangt der Fördermittelgeber? (Formular, Freitext, Anhänge?)
- [ ] **Struktur des Zwischenberichts** festlegen – typische Elemente:
  - Projektstand und Meilensteine
  - Methodik (Framework, empirische Evaluationskette)
  - Bisherige Ergebnisse (Workshops, erste Erkenntnisse)
  - Nächste Schritte und Zeitplan
  - Ressourcenverbrauch
- [ ] Entscheiden, welche der bestehenden Texte direkt in den Zwischenbericht einfließen (Auszüge aus dem Leitfaden, Framework-Beschreibung aus dem PDF)
- [ ] **Workshop-Dokumentation** ist Kerninhalt des Zwischenberichts – muss vorher fertig sein (→ A1)
- [ ] Zwischenbericht als separates Dokument erstellen (eigene LaTeX-Datei oder Word, je nach Vorgabe)

---

## G · Offene konzeptionelle Fragen (zur Klärung)

- [ ] **Zielbeziehung der beiden Hauptdokumente**: Wie verhalten sich der Leitfaden (praxisorientiert für KMU) und das Framework (Forschungsinstrument) zueinander? Klare Rollentrennung formulieren
- [ ] **Begleitendes Software-Tool** (im Leitfaden erwähnt): Existiert dieses Tool? Ist es geplant? Soll es im Projekt entwickelt werden?
- [ ] **Geografischer Fokus**: Der Leitfaden betont Flensburg/Grenzgebiet DK-DE – ist das für den Zwischenbericht zentral oder eher Hintergrundkontext?
- [ ] **Weitere Workshops geplant?**: Das Framework sieht mehrere Anwendungsstudien vor (5 Meeting-Typen). Sind nach dem Verhandlungs-Workshop weitere Szenarien geplant? Welche Typen haben Priorität?
- [ ] **Quellennachweis im PDF**: Quelle [6] mit „??" – Fehler bewusst oder versehentlich? Bereinigen

---

---

## H · Eigene Feldexperimente (neu · März 2026)

> Diese Experimente wurden durchgeführt, sind aber noch nicht im Buchmanuskript verarbeitet. Sie müssen in `Buch/06_empirische_untersuchung.md` oder in einem neuen Anhang-Kapitel dokumentiert und im Framework verortet werden.

### H1 · LIDAR-Scanning mit iPhone 15 Pro

- [x] **Experiment durchgeführt** (zwei iPhone 15 Pro genutzt)
- **Ergebnis**: LIDAR-basiertes Innenraum-Scanning auf Consumer-Hardware ist derzeit **zu unreif** für den professionellen Einsatz. Details in VR zur gemeinsamen Besprechung (z. B. Raumdetails, Oberflächenqualitäten) sind unzureichend darstellbar.
- [ ] Ergebnisbeschreibung in `Buch/06_empirische_untersuchung.md` einfügen (kurze Negativ-Fallstudie: was wurde getestet, warum ungeeignet, Handlungsempfehlung: aktuell nicht empfehlenswert)
- [ ] Framework-Verortung: TI (Datenerfassung), VA (VR-Eignung für Raumanalyse-Meetings)
- [ ] Relevanz für Testfall F03 (Sportbootgutachter) dokumentieren
- **Testfall-Relevanz**: F03 (Bootsgutachter), F09 (Architekturbüro), F04 (Maschinenbauer)

### H2 · 360°-Fotografie für Wert- und Schadensgutachten (Sportboote)

- [x] **Experiment durchgeführt** in Zusammenarbeit mit **Stefan Bruns, sportboot-gutachter.de**
- **Ansatz**: 360°-Fotos von Booten in VR zur gemeinsamen Begutachtung und Verhandlung von Schäden/Werten über Distanz
- [ ] Fallstudie dokumentieren: Aufbau, Vorgehen, Beobachtungen, Bewertung
- [ ] Stefan Bruns als Referenz / Ansprechpartner benennen: sportboot-gutachter.de
- [ ] Einordnung: Wo ist 360°-Foto-VR geeignet, wo sind die Grenzen gegenüber LIDAR/Photogrammetrie?
- [ ] In Framework verorten: VA (Remote-Inspektion als Meeting-Typ), TI (360°-Foto-Pipeline), EU (zweite Anwendungsstudie)
- [ ] In `Buch/06_empirische_untersuchung.md` als Praxisexperiment aufnehmen
- **Testfall-Relevanz**: F03 (Bootsgutachter), F02 (Werft), F12 (Windenergie-Inspektion)

### H3 · VR-Messestand

- [x] **Experiment durchgeführt** in Zusammenarbeit mit:
  - **Orion** (Ansprechpartner und Kontext prüfen)
  - **Omnicon Group** (Flensburg-Umgebung)
  - **Neox Studios** (Flensburg)
- [ ] Fallstudie dokumentieren: Konzept, Umsetzung, Plattform, Beobachtungen
- [ ] Referenz-Ansprechpartner bei Orion/Omnicon/Neox für Publikation klären (Einverständnis)
- [ ] Bewertung: Wo war VR-Messestand überzeugend, wo lagen Grenzen?
- [ ] Framework-Verortung: VA (Marketing/Präsentation als Meeting-Typ), BN (Customer Experience, Employer Branding), TI
- [ ] In `Buch/06_empirische_untersuchung.md` oder neues Kapitel `Buch/Workshop/messestand.md`
- **Testfall-Relevanz**: F07 (Messebauagentur), F10 (Tourismus), F15 (Einzelhandel)

### H4 · Muse S EEG-Headband-Experiment (abgebrochen / negatives Ergebnis)

- [x] **Experiment geplant und teilweise durchgeführt**
- **Ziel**: Stressmessung während VR-Meeting-Aufgaben via EEG-Daten
- **Ergebnis**: Experiment **nicht weitergeführt** aus folgenden Gründen:
  - EEG-Datenintegration technisch aufwändig; keine einfache API-Anbindung an VR-Systeme
  - Muse S ist primär für Entspannungs-/Meditationsanwendungen konzipiert — für Stressmessung in kognitiv fordernden Tasks ungeeignet (zu wenig Kanäle, zu viel Artefaktrauschen bei Bewegung)
  - Valide Stressmessung würde klinische EEG-Hardware, Signalverarbeitung und Expertise erfordern, die im Projektrahmen nicht verfügbar war
- [ ] Kurzdarstellung des negativen Ergebnisses in `Buch/06_empirische_untersuchung.md` aufnehmen (als Methodenreflexion: Was wurde erwogen, warum verworfen)
- [ ] Handlungsempfehlung: Für KMU-Kontexte derzeit **nicht empfehlenswert**; bei wissenschaftlichem Interesse Verweis auf validierte Forschungs-EEG-Setups
- [ ] Framework-Verortung: TI (Datenerfassung, KI Assistenzsystem), EU (Messmethodik), WB (Hypothesen zu Stress)
- **Testfall-Relevanz**: F06 (Pflegeeinrichtung — Stressbelastung Pflegekräfte), F12 (Windenergie — Stressbelastung Sicherheitstraining)

### H5 · KI-Avatar in Verhandlungssituation (geplant)

- [ ] **Nächste geplante Fallstudie**: Verhandlungsszenario aus dem Workshop (Kap. 06) wird erweitert um einen **KI-gesteuerten Avatar** als Verhandlungspartner
- **Forschungsfragen**:
  - Verändert ein KI-Avatar die Verhandlungsstrategie der menschlichen Teilnehmer?
  - Wird der Avatar als gleichwertiger Verhandlungspartner wahrgenommen?
  - Welche spieltheoretischen Vorhersagen gelten für Mensch-KI-Verhandlungen vs. Mensch-Mensch?
- [ ] Experiment planen und durchführen
- [ ] Spieltheoretisches Modell (Kap. Workshop/spieltheorie.md) auf Mensch-KI-Konstellationen anpassen
- [ ] Framework-Verortung: VA (Meeting-Typ: Verhandlung), WB (Hypothesen), TI (KI Assistenzsystem), EU
- **Testfall-Relevanz**: F08 (Kanzlei — KI-Mediationsassistent?), F04 (Maschinenbauer — KI-Verhandlungscoach?)

---

## I · Datenschutz und DSGVO-Compliance (neu · kritisch)

### I1 · Meta Quest DSGVO-Analyse

- [ ] **Explizites Kapitel oder Einschub in `Buch/08_technische_implementation.md`** zum Thema Meta Quest und DSGVO
- **Kern der Problematik**:
  - Meta Platforms ist ein US-Unternehmen; Daten unterliegen dem CLOUD Act (US-Regierungszugriff möglich)
  - Biometrische Daten (Augenbewegungen, Handgesten, Stimme) werden auf Meta-Servern verarbeitet
  - Nutzungsbedingungen erlauben Datenverwendung für Werbezwecke — unvereinbar mit professionellen Kontexten
  - Keine On-Premise-Option für Meta Quest: auch der „Gast-Modus" sendet Telemetriedaten
  - Schrems-II-Entscheidung (EuGH 2020): Datentransfer in die USA ohne angemessenes Schutzniveau problematisch
- **Konsequenz für das Buch**: Für alle Kontexte mit personenbezogenen oder vertraulichen Daten muss Meta Quest als **datenschutzrechtlich nicht empfehlenswert** eingestuft werden
- **Betroffene Branchen**: Medizin, Recht, Steuerberatung, Behörden, alle Kontexte mit Betriebsgeheimnissen
- **Testfall-Relevanz**: F06, F08, F13, F18 (kritische Lücke)

### I2 · DSGVO-konforme VR-Hardware-Alternativen

- [ ] Recherchieren und in `Buch/08_technische_implementation.md` dokumentieren:
  - **Pico (ByteDance)**: chinesische Eigentümerschaft — ebenfalls problematisch für viele Kontexte
  - **HTC Vive Focus** (PC-tethered oder Stand-alone): Enterprise-Option mit DSGVO-Anpassungen möglich
  - **Varjo (VR-1/XR-4)**: finnisches Unternehmen, EU-basiert, Enterprise-DSGVO-Compliance-Optionen
  - **PC-tethered + OpenVR** (HTC Vive, Valve Index): lokale Datenhaltung vollständig möglich — aufwändiger, aber datenschutzkonform
  - **WebXR mit eigenem Server**: kein Headset-Account nötig, vollständige Datenkontrolle
- [ ] Entscheidungsbaum: „Welches Headset für welchen Kontext?" — datenschutzbasiert

### I3 · ULD Schleswig-Holstein als regionale Aufsichtsbehörde

- [ ] ULD (Unabhängiges Landeszentrum für Datenschutz Schleswig-Holstein) als maßgebliche Aufsichtsbehörde für SH-Unternehmen in `Buch/08_technische_implementation.md` oder `Buch/10_implementierungsleitfaden.md` nennen
- [ ] ULD-Position zu biometrischer Datenverarbeitung in VR referenzieren (falls Stellungnahme vorhanden)
- [ ] Hinweis: Für datenschutzrechtliche Fragen empfiehlt sich Vorabkonsultation beim ULD (kostenlos für Unternehmen in SH)

---

## J · Testfälle als Buchdeckungsanalyse

- [x] 20 Testfall-Organisationen aus SH erstellt: `Buch/testcases_coverage.md`
- [ ] Priorisierte Lücken aus Testfall-Analyse systematisch schließen (s. Lückenmatrix in der Datei)
- [ ] Nach jedem größeren Buchkapitel-Update: Testfälle erneut gegen Buchdeckung prüfen
- [ ] Entscheiden, welche Testfälle als **anonymisierte Vignetten** in den Leitfaden selbst integriert werden können

### Kritische Lücken aus Testfallanalyse (sofort adressieren)

| Priorität | Lücke | Betroffene Fälle | Maßnahme |
|---|---|---|---|
| 🔴 Kritisch | Meta Quest DSGVO-Inkompatibilität | F06, F08, F13, F18 | → I1, I2 |
| 🔴 Kritisch | Berufsgeheimnisschutz (Anwalt, Arzt, Steuer) | F08, F13, F18 | Einschub Kap. 08/10 |
| 🔴 Kritisch | Eigene Experimente nicht eingearbeitet | F03, F07 | → H1, H2, H3 |
| 🟡 Wichtig | Betriebsrat / § 87 BetrVG bei VR-Einführung | F14 | Einschub Kap. 03/10 |
| 🟡 Wichtig | Mehrsprachige VR-Inhalte | F02, F05, F16 | Kap. 04 oder 07 |
| 🟡 Wichtig | Hygiene-Konzept Headset-Sharing | F11, F18 | Kap. 08 |
| 🟡 Wichtig | SH-spezifische Förderprogramme | alle | neuer Anhang |
| 🟡 Wichtig | ROI für Kleinstbetriebe <10 MA | F01, F03, F05 | Kap. 03 |
| 🟢 Mittelfristig | Maritime Regulierung (STCW) | F19 | Kap. 04/08 |
| 🟢 Mittelfristig | Medizinrecht MDR für VR | F06, F18 | Kap. 04/08 |
| 🟢 Mittelfristig | VR als Dienstleistungsmodell | F07, F17 | Kap. 03 |

---

## Priorisierungsvorschlag

| Priorität | Aufgaben |
|-----------|----------|
| **Sofort** (für Zwischenbericht) | A1, A2, F, H1, H2, H3, I1 |
| **Kurzfristig** (inhaltliche Basis) | B1, B2, C3, D1, H4, H5, I2, I3, J |
| **Mittelfristig** (Konsistenz) | A3, C1, C2, D2, E |
| **Langfristig** (Vollständigkeit) | B1 (vertieft), G |
