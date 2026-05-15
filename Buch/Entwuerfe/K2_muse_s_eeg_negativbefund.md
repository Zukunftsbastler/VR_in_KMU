# Entwurf: Muse S EEG-Headband — Methodenreflexion (Negativbefund)

> **Zielstelle im Buch:** `Buch/06_empirische_untersuchung.md`
> Einzufügen als neuer Abschnitt **nach** dem bestehenden Abschnitt „Verhaltensbeobachtung (CIPD-Kodierung)",
> vor einem ggf. folgenden Abschnitt zu Experiment H1 (LIDAR-Scanning) oder H2 (360°-Fotografie).
> Überschriftenebene: `##` (gleichwertig mit „Studiendesign", „Ergebnisse" etc.)
>
> **Charakter:** Methodenreflexion — kein durchgeführtes Experiment, sondern eine erwogene und
> begründet verworfene Erweiterung des Messinstrumentariums.
>
> **Framework-Verortung:** TI (Datenerfassung, KI-Assistenzsysteme), EU (Messmethodik),
> WB (Hypothesen zu Stress und kognitiver Belastung)
> **Testfall-Relevanz:** F06 (Pflegeeinrichtung — Stressbelastung Pflegekräfte),
> F12 (Windenergie — Stressbelastung im Sicherheitstraining)

---

## Methodenreflexion: EEG-gestützte Stressmessung (Muse S — Negativbefund)

### Ausgangsfrage und Überlegung

Im Verlauf der Experimentplanung entstand die Frage, ob sich das Stressniveau der Teilnehmer während VR-gestützter Verhandlungsaufgaben über physiologische Messverfahren erfassen lässt. Die Motivation war naheliegend: Subjektive Selbstauskünfte — wie sie die eingesetzten Kurzinstrumente ATI-S, FMS und UEQ-S liefern — setzen voraus, dass Teilnehmer ihre inneren Zustände korrekt wahrnehmen und verbal beschreiben können. Eine objektive, kontinuierliche Stressmessung hätte eine von der Selbsteinschätzung unabhängige Datenschicht erzeugt.

Als Kandidat für ein niedrigschwelliges Consumer-EEG-Gerät wurde das **Muse S** (InteraXon Inc.) geprüft. Das Gerät ist für den Endverbrauchermarkt konzipiert, als Stirnband tragbar und verspricht eine einfache Handhabung ohne klinische Expertise.

### Bewertung und Gründe für den Verzicht

Die Prüfung ergab, dass die Technologie für den angestrebten Anwendungsfall nicht geeignet ist. Die Gründe lassen sich auf drei Ebenen systematisieren:

**1. Konzeptionelle Fehlanpassung: Gerät und Aufgabe passen nicht zusammen**

Das Muse S ist primär für **Entspannungs- und Meditationsanwendungen** konzipiert. Die zugehörige Referenzdatenbank, auf der die Echtzeitfeedback-Algorithmen basieren, ist für Ruhezustandsmessungen kalibriert. Kognitive Aufgaben mit simultaner Interaktion — wie eine mehrphasige Verhandlung in VR — erzeugen EEG-Aktivitätsmuster, für die das Gerät keine validierten Auswertungsroutinen bereithält. Das Gerät misst, aber das Ergebnis ist nicht interpretierbar.

**2. Technische Limitierungen: Kanalzahl und Bewegungsartefakte**

Valide EEG-Messungen erfordern eine ausreichende Anzahl von Elektroden (Kanälen), um kortikale Aktivität räumlich aufzulösen und Artefaktsignale herausfiltern zu können. Das Muse S verfügt über lediglich **vier EEG-Kanäle** (Fp1, Fp2, TP9, TP10), die ausschließlich frontale und temporale Bereiche abdecken. Für die Messung von Stressreaktionen und kognitiver Belastung werden in der Forschungsliteratur typischerweise 32 bis 64 Kanäle eingesetzt, um relevante Frequenzbänder (Alpha, Beta, Theta) zuverlässig zu trennen.

Hinzu kommen **Bewegungsartefakte**: In einer VR-Umgebung, in der Teilnehmer ihren Kopf wenden, mit Avataren interagieren und Gesten ausführen, produzieren Muskelaktivitäten (EMG) und Kopfbewegungen Signalstörungen, die die schwachen EEG-Signale in derselben Frequenzgröße überlagern. Die Artefaktbereinigung erfordert spezialisierte Signalverarbeitungssoftware (z. B. Independent Component Analysis, ICA) und Expertenwissen, die im Projektrahmen nicht zur Verfügung standen.

**3. Infrastrukturelle Anforderungen: Keine direkte API-Integration in VR-Systeme**

Eine sinnvolle Auswertung würde eine zeitlich synchronisierte Aufzeichnung von EEG-Signal und VR-Ereignissen erfordern — d. h. welche Verhandlungsrunde, welches Gebot, welche Reaktion eines Avatars läuft parallel zu welchem Stresssignal. Die Einbindung des Muse S in die Unity-Spielumgebung über das Muse SDK (OSC-Protokoll) ist technisch möglich, erfordert jedoch eine nichttriviale Middleware-Entwicklung. Die Datenqualität (s. o.) hätte diesen Entwicklungsaufwand nicht gerechtfertigt.

### Einordnung und Handlungsempfehlung

Der Verzicht auf die EEG-Messung ist kein Qualitätsmangel des Studiendesigns, sondern das Ergebnis einer bewussten Abwägung. Stressmessung per EEG ist ein legitimes Forschungsziel — aber eines, das spezifische Voraussetzungen mitbringt, die über den Rahmen eines praxisorientierten KMU-Transferprojekts hinausgehen.

**Für KMU-Entscheider:** EEG-basierte Stressmessung ist im betrieblichen Alltag derzeit **nicht als niedrigschwelliges Hilfsmittel** zur Bewertung von VR-Anwendungen einsetzbar. Consumer-Geräte wie das Muse S sind für Meditationsanwendungen valide, nicht jedoch für kognitive Belastungsmessungen in interaktiven Aufgabenumgebungen.

**Für wissenschaftliche Anschlussprojekte:** Wer EEG-gestützte Stressmessung in VR valide durchführen möchte, benötigt:

- **Forschungs-EEG-Hardware** mit mindestens 32 Kanälen (z. B. Brain Products actiCAP, Emotiv EPOC X in der Forschungsversion, g.tec g.USBamp)
- **Signal-Preprocessing-Pipeline** (EEGLab/MNE-Python) mit Artefaktbereinigung und ICA
- **Synchronisiertes Event-Marking** zwischen EEG-Aufzeichnungssoftware und VR-Anwendung (z. B. über LSL — Lab Streaming Layer)
- **Fachkundige Begleitung** durch Neurowissenschaftler oder kognitive Psychologen für Paradigmenentwurf und Auswertung

Mit diesem Setup wären Fragestellungen zu **kognitiver Überbelastung in VR-Meetings**, **Hemisphärenaktivierung bei Verhandlungsstrategien** oder **Immersionstiefe als neuronales Korrelat** grundsätzlich untersuchbar — allerdings mit erheblichem Mehraufwand gegenüber dem vorliegenden Projektzuschnitt.

> **Methodische Transparenz:** Das Abwägen und begründete Verwerfen eines Messinstruments ist Teil eines sorgfältigen Forschungsprozesses. Dieser Abschnitt dokumentiert nicht ein Scheitern, sondern ein informiertes Urteil: Das richtige Werkzeug für die falschen Bedingungen einzusetzen, würde die Qualität der Ergebnisse nicht erhöhen, sondern senken.

---

### Ausblick: Wearable-Physiologie als künftige Ergänzungsschicht

Auch wenn das Muse S für EEG-Stressmessung ungeeignet ist, eröffnet die Wearable-Physiologie mittelfristig andere, realistischere Zugänge zur objektiven Zustandsmessung in VR-Experimenten:

| Methode | Gerät (Beispiel) | Stärken | Grenzen |
|---------|-----------------|---------|---------|
| **Herzratenvariabilität (HRV)** | Polar H10, Garmin-Brustgurt | Valider Stressindikator, störungsrobust, einfache API-Anbindung | Verzögertes Signal (Minuten, nicht Sekunden) |
| **Elektrodermale Aktivität (EDA/GSR)** | Empatica E4, Shimmer3 GSR+ | Sensitiv für kurzfristige Erregungsveränderungen | Anfällig für Bewegungsartefakte an der Hand |
| **Eye-Tracking (integriert)** | Meta Quest Pro, Varjo XR-4 | Pupillendurchmesser als kognitiver Belastungsindikator; direkt in VR-Hardware integriert | Nur in Premium-Hardware verfügbar; Kalibrierung nötig |

Von diesen Optionen ist **Eye-Tracking** besonders vielversprechend für den vorliegenden Kontext: Premium-VR-Headsets wie die Meta Quest Pro oder Varjo XR-4 integrieren Eye-Tracking bereits in die Hardware. Pupillendurchmesser und Fixationsmuster sind valide Korrelate kognitiver Belastung (Kahneman, 1973; Van der Wel & Van Steenbergen, 2018) und ließen sich ohne zusätzliche Hardware synchron zur VR-Interaktion aufzeichnen. Für zukünftige Workshop-Iterationen, die auf datenschutzkonformer Hardware (→ Kap. 08) basieren, empfiehlt sich die Prüfung dieses Ansatzes.
