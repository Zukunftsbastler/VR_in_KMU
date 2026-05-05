# 3. Fortschritt der Arbeitspakete

---

## AP 1: Framework Meeting Types

**Beschreibung laut Antrag:** Literaturrecherche; existierende Meeting-Typen durch
Grounded Theory strukturieren.

**Status: ✅ Abgeschlossen**

Die Literaturrecherche umfasst Technologieakzeptanzmodelle (UTAUT, Venkatesh et al. 2003),
Präsenzforschung, spieltheoretische Grundlagen sowie empirische Studien zu VR-Meetings
und kollaborativer Zusammenarbeit. Eine kommentierte Bibliographie (`literatur.bib`) wurde
aufgebaut und um peer-reviewed Studien zu VR-Verhandlungen ergänzt.

Auf dieser Grundlage wurde eine **Meeting-Taxonomie** mit acht Bewertungsdimensionen
entwickelt (u. a. Entscheidungstiefe, Interaktionsbedarf, Vertraulichkeit, Teilnehmerzahl).
Für jeden Meeting-Typ wurde eine VR-Eignungsbewertung auf einer fünfstufigen Skala (★–★★★★★)
erarbeitet. Die Taxonomie integriert Erkenntnisse aus der Literatur mit Befunden aus dem
eigenen Workshop-Experiment und bildet das Rückgrat des Sieben-Domänen-Frameworks.

Ergänzend wurde ein **Hypothesenkatalog (H1–H18)** entwickelt, der die zentralen
Forschungsannahmen des Projekts multidisziplinär fundiert und mit Literaturbelegen versieht.

---

## AP 2: Leitfaden erarbeiten

**Beschreibung laut Antrag:** Framework zur Beschreibung von Meetings; Ermöglichen einer
realistischen Kostenschätzung durch die Analogiemethode; Aufzeigen von Herausforderungen.

**Status: ✅ Weit fortgeschritten (Manuskript vollständig, Restpunkte in Bearbeitung)**

Das zentrale Transferprodukt — ein **praxisorientiertes Handbuch für KMU-Entscheider** —
liegt als vollständig strukturiertes Buchmanuskript in neunzehn Markdown-Kapiteln vor
(Rendering via Quarto + Typst). Die Kapitelstruktur folgt dem Sieben-Domänen-Framework:

| Kapitel | Inhalt | Status |
|---------|--------|--------|
| Kap. 01 | Einführung, Zielsetzung, Zielgruppe | ✅ |
| Kap. 02 | Sieben-Domänen-Framework | ✅ |
| Kap. 03 | Betriebswirtschaftlicher Nutzen (inkl. Analogiemethode zur Kostenschätzung) | ✅ |
| Kap. 04 | Anwendungsszenarien (Meeting-Taxonomie, belegte Fallstudien) | ✅ |
| Kap. 05 | Wissenschaftliche Basis (UTAUT, Spieltheorie) | ✅ |
| Kap. 06 | Empirische Untersuchung | ✅ (Feldexperimente werden ergänzt) |
| Kap. 07 | Person und Individuum | ✅ |
| Kap. 08 | Technische Implementation | ⚠️ DSGVO-Analyse Meta Quest ausstehend |
| Kap. 09 | Trends und Zukunft | ✅ |
| Kap. 10 | Implementierungsleitfaden | ✅ |
| Anhang A–D | Glossar (37 Begriffe), Checklisten, Messinstrumente, Ressourcen | ✅/⚠️ |

Herausforderungen für den KMU-Einsatz von VR sind im Leitfaden umfassend aufgezeigt:
Investitionskosten, Motion-Sickness-Risiko, Datenschutz (insbesondere Meta Quest),
Schulungsaufwand und fehlende IT-Support-Strukturen. Als Qualitätssicherungsmaßnahme
wurden 16 fiktive Fallstudien identifiziert und durch belegte Praxisfälle ersetzt.

---

## AP 3: Beispielprojekte beschreiben

**Beschreibung laut Antrag:** UTAUT zur Einordnung der Probanden; Pilotprojekte/Experimente
mit konkreten Meeting-Typen; Interviews zur Einordnung der Erkenntnisse.

**Status: ✅ Kernstudie abgeschlossen / 🔄 Feldexperimente laufend**

### Unity-Applikation (Forschungsplattform)

Als Grundlage für alle Pilotprojekte wurde eine **Unity-basierte VR-Multiplayer-Applikation**
nach dem Principal-Agent-Paradigma entwickelt. Die Applikation bildet ein
Unternehmens-Verhandlungsszenario ab, in dem drei Teilnehmende als Führungskräfte über die
Verteilung strategischer Ressourcen verhandeln. Der Quellcode ist öffentlich verfügbar:
https://github.com/phillipja/BeyondRealityResearch

<!-- TODO: Eingesetzte VR-Hardware angeben (z. B. Meta Quest 2/3, Anzahl der Headsets).
     Falls im Finanzbericht Hardware-Ausgaben abgerechnet werden, hier erwähnen. -->

### Workshop-Experiment: VR-Verhandlungsstudie (n=15)

<!-- TODO: Genaues Durchführungsdatum / Semester eintragen -->

**Probanden-Einordnung (UTAUT-Referenz):** Die Technikaffinität wurde mit der ATI-Kurzskala
(3 Items, Skala 1–6) erhoben. Die Stichprobe (BWL-Erstsemester, Studiengang „Digitale
Wirtschaft") zeigte mittlere Gesamtaffinität mit hoher Streuung — ein für KMU-Belegschaften
typisches Muster.

**Messinstrumente:** ATI-Kurzskala, FMS (Motion Sickness), UEQ-S (User Experience),
Verhaltensbeobachtung nach CIPD-Kodierung, qualitative Kurzinterviews.

**Zentrale Befunde:**

- **Hohe hedonische Qualität:** UEQ-S ∅ 6,18/7 (hedonisch) vs. ∅ 5,53/7 (pragmatisch);
  das Item „neuartig" erreichte M=6,67/7 — nahezu universell bestätigt.
- **Immersion:** 28 % aller codierten Aussagen (n=102 aus Kurzinterviews) entfielen auf
  Immersionserlebnisse; Teilnehmende beschrieben das Vergessen der physischen Umgebung.
- **Natürliche Interaktion:** Deiktische Gesten und soziale Zuwendung wurden auch bei
  physisch getrennten Teilnehmenden beobachtet — VR aktiviert Präsenz-Muster des
  Präsenztreffens auch über Distanz.
- **Motion Sickness:** 38 % der Teilnehmenden wiesen nach der Session erhöhte FMS-Werte auf;
  ein Extremfall (FMS=20) erfordert proaktive Screening-Protokolle.
- **Praxispotenzial:** Genannte geeignete Szenarien: Kreativ-Workshops, Strategie-Meetings,
  Lernveranstaltungen. Weniger geeignet: Routine-Kommunikation.

### Praxisexperiment H1: LIDAR-Scanning (Negativbefund)

Erprobt wurde, ob iPhones mit LIDAR-Sensor (iPhone 15 Pro, 3D Scanner App) für die Erstellung
VR-tauglicher 3D-Scans von Objekten und Räumen geeignet sind. Das Ergebnis war ein klarer
Negativbefund: Detailverlust, Loch-Artefakte und physikalisch bedingte Transparenzprobleme
machen Consumer-LIDAR für professionelle VR-Inhalte aktuell ungeeignet. Der Befund fließt
direkt als Handlungsempfehlung in den Leitfaden ein.

### Praxisexperiment H2: 360°-Fotografie (Fallstudie Sportbootgutachten)

Als niedrigschwellige Alternative zu LIDAR wurde 360°-Fotografie (Insta360-Kamera) in
Zusammenarbeit mit einem Fachgutachter (sportboot-gutachter.de) erprobt. Die Aufnahmen
des Motorboots „Albin Köbis" wurden als Skybox-Navigation mit Points of Interest in eine
Unity-VR-Applikation integriert. Die Nutzertests und abschließende Bewertung durch den
Praxispartner stehen noch aus.

<!-- TODO: Einverständnis zur namentlichen Nennung (Stefan Bruns / sportboot-gutachter.de)
     bestätigt? Anzahl Aufnahmepositionen und VR-Hardware beim Test eintragen. -->

### Praxisexperiment H3: Virtueller Messestand

<!-- TODO: Details ergänzen:
- Welche Partner haben teilgenommen (Einverständnis zur Nennung)?
- Wann fand das Experiment statt?
- Gibt es bereits Beobachtungen oder erste Ergebnisse? -->

Erprobt wurde ein vollständig virtuelles Messeszenario in Unity, bei dem Partnerunternehmen
ihre Produkte an virtuellen Messeständen präsentieren. Nutzertests und Auswertung laufen noch.

---

## AP 4: Projektmanagement

**Status: ✅ Laufend**

Koordination der Arbeitspakete, Abstimmung mit Praxispartnern, Betreuung des
Softwareentwicklungs-Repositories sowie laufende Dokumentation des Projektfortschritts.

<!-- TODO: Falls studentische Hilfskräfte oder externe Mitarbeitende eingesetzt wurden
     und im Finanzbericht abgerechnet werden, hier kurz erwähnen. -->
