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

Als Nebenprodukt entstanden in dieser Phase die strukturellen Grundlagen des geplanten
Praxisleitfadens (→ AP 2).

---

## AP 2: Leitfaden erarbeiten

**Beschreibung laut Antrag:** Framework zur Beschreibung von Meetings; Ermöglichen einer
realistischen Kostenschätzung durch die Analogiemethode; Aufzeigen von Herausforderungen.

**Status: 🔄 In Bearbeitung — Grundstruktur im Berichtszeitraum angelegt, Ausarbeitung läuft (ab 2026)**

Im Berichtszeitraum wurde die Grundstruktur des zentralen Transferprodukts — eines
**praxisorientierten Handbuchs für KMU-Entscheider** — als Buchmanuskript in neunzehn
Markdown-Kapiteln angelegt (Rendering via Quarto + Typst). Die Kapitelstruktur folgt dem
Sieben-Domänen-Framework; der aktuelle Bearbeitungsstand (Mai 2026) ist der folgenden
Tabelle zu entnehmen:

| Kapitel | Inhalt | Status |
|---------|--------|--------|
| Kap. 01 | Einführung, Zielsetzung, Zielgruppe | ✅ |
| Kap. 02 | Sieben-Domänen-Framework | ✅ |
| Kap. 03 | Betriebswirtschaftlicher Nutzen (inkl. Analogiemethode zur Kostenschätzung) | ✅ |
| Kap. 04 | Anwendungsszenarien (Meeting-Taxonomie, belegte Fallstudien) | ✅ |
| Kap. 05 | Wissenschaftliche Basis (UTAUT, Spieltheorie) | ✅ |
| Kap. 06 | Empirische Untersuchung | ✅ (Feldexperiment-Befunde werden ergänzt) |
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

**Status: ✅ Kernstudie abgeschlossen / 🔄 Integration von Vorläuferprojekt-Befunden läuft (2026)**

### Praxisexperiment H1: LIDAR-Scanning (Negativbefund)

Erprobt wurde, ob iPhones mit LIDAR-Sensor für die Erstellung VR-tauglicher 3D-Scans von
Objekten und Räumen geeignet sind. Als Testgeräte wurden zwei iPhone 15 Pro eingesetzt, die
explizit für dieses Projekt angeschafft wurden. Die Entscheidung für Apple-Hardware folgte
einem bewussten Kriterium: Das iPhone ist in KMU-Belegschaften weit verbreitet, sodass eine
etwaige Reproduzierbarkeit der Ergebnisse ohne zweckgebundene Spezialhardware gewährleistet
ist — ein zentrales Argument für die Übertragbarkeit auf den Mittelstand.

Die Scans wurden mit der App „3D Scanner App" durchgeführt. Das Ergebnis war ein klarer
Negativbefund: Detailverlust, Loch-Artefakte und physikalisch bedingte Transparenzprobleme
machen Consumer-LIDAR für professionelle VR-Inhalte aktuell ungeeignet. Der Befund fließt
direkt als Handlungsempfehlung in den Leitfaden ein.

### Unity-Applikation (Forschungsplattform)

Als Grundlage für alle weiteren Pilotprojekte wurde eine **Unity-basierte
VR-Multiplayer-Applikation** nach dem Principal-Agent-Paradigma entwickelt. Die Applikation
bildet ein Unternehmens-Verhandlungsszenario ab, in dem drei Teilnehmende als Führungskräfte
über die Verteilung strategischer Ressourcen verhandeln. Der Quellcode wird in einem privaten GitHub-Repository verwaltet:
https://github.com/phillipja/BeyondRealityResearch

### Workshop-Experiment: VR-Verhandlungsstudie (n=15)

**Durchführungszeitraum:** 13. November – 2. Dezember 2025

**Eingesetzte VR-Hardware:** Zwei Meta Quest Pro und eine Meta Quest 3 — diese Geräte waren
bereits vor Projektbeginn vorhanden und wurden nicht eigens für dieses Projekt angeschafft.

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

### Ergänzende Fallstudien aus Vorläuferprojekt (Integration in 2026)

Zwei weitere Praxisprojekte wurden im Rahmen eines Vorläuferprojekts durchgeführt, jedoch
bislang nicht ausgewertet: eine **360°-Fotografie-Anwendung** auf Basis von
Skybox-Technologie für Besichtigungsszenarien sowie ein **VR-Messestand-Experiment** mit
einem Gestenperzeptionstest (N=12, 45 Gesten, 0 % Fehlerquote). Da die Befunde beider
Projekte auf den KMU-Einsatz von VR übertragbar sind, fließen sie als Praxisbeispiele in
den abschließenden Leitfaden ein und werden in der verbleibenden Projektlaufzeit
eingearbeitet.

---

## AP 4: Projektmanagement

**Status: ✅ Laufend**

Koordination der Arbeitspakete, Abstimmung mit Praxispartnern, Betreuung des
Softwareentwicklungs-Repositories sowie laufende Dokumentation des Projektfortschritts.
