---
title: "Workshop-Szenario"
---

## Überblick

Der Workshop simuliert eine Führungskräftekonferenz eines mittelständischen Technologieunternehmens in einer vollständig immersiven VR-Umgebung. Drei Teilnehmer nehmen gleichzeitig teil – jeder sitzt allein in einem separaten physischen Raum und tritt über VR-Avatare in Kontakt. Das Verhandlungsziel: die Verteilung strategischer Ressourcen für das kommende Geschäftsjahr.

## Rahmenbedingungen

Das Unternehmen steht an einem strategischen Scheideweg. Die verfügbaren Ressourcen sind begrenzt:

- **Gesamtbudget:** 10 Mio. €
- **Personalkapazität:** 50 Vollzeitäquivalente (VZÄ)
- **IT-Ressourcen:** 1.000 Servereinheiten

Jede Führungskraft vertritt eine Abteilung mit eigenen Zielen, Prioritäten und – entscheidend – **privaten Informationen**, die die anderen nicht kennen.

## Rollen

### Forschungsleiterin (Dr. Sarah Chen)

Dr. Sarah Chen leitet die Forschungs- und Entwicklungsabteilung. Ihre Priorität liegt auf Investitionen in technologische Innovationen, insbesondere im Bereich Quantencomputing. Sie besitzt interne Erkenntnisse über vielversprechende Forschungsergebnisse, die für das Unternehmen transformative Bedeutung haben könnten – sofern ausreichend Ressourcen bereitgestellt werden.

**Verhandlungsinteressen:** Hoher F&E-Budgetanteil, moderate Personalkapazität, geringe IT-Serverkapazität.

### Vertriebsleiter (Marcus Weber)

Marcus Weber verantwortet den nationalen und internationalen Vertrieb. Er verfügt über Informationen zu einem potenziellen Großauftrag, der kurzfristig erhebliche Umsätze generieren könnte – aber nur, wenn das Vertriebsteam personell und technisch ausreichend ausgestattet ist.

**Verhandlungsinteressen:** Moderates Budget, hohe Personalkapazität (Vertriebsfokus), substanzielle IT-Ressourcen für CRM und Kommunikation.

### Finanzvorstand (Thomas Bauer)

Thomas Bauer trägt die Gesamtverantwortung für die finanzielle Stabilität des Unternehmens. Er kennt Details zu bevorstehenden regulatorischen Änderungen, die erhebliche Compliance-Kosten verursachen werden. Er muss zwischen Investitionen in Wachstum und der Absicherung gegen regulatorische Risiken abwägen.

**Verhandlungsinteressen:** Ausgewogene Ressourcenverteilung, starke Berücksichtigung langfristiger Unternehmensrisiken.

## Ablauf

### Phase 1: Vorbereitung (30 Minuten)

- Einzel-Briefing jedes Teilnehmers mit Rollenbeschreibung und privaten Informationen
- ATI-Kurzfragebogen (3 Items) zur Erfassung der Technikaffinität
- FMS-Fragebogen (Baseline für Motion Sickness)

### Phase 2: VR-Onboarding (15 Minuten)

- Einführung in die VR-Umgebung (Navigation, Avatar-Steuerung, Interaktion)
- Kalibrierung der Hardware
- Kurze Orientierungsrunde im virtuellen Konferenzraum

### Phase 3: Verhandlung (45–60 Minuten)

Die Verhandlung findet in mehreren Runden statt. Nach jeder Runde können Allianzen neu gebildet, Informationen strategisch offenbart und Angebote angepasst werden. Die Fortsetzungswahrscheinlichkeit sinkt mit jeder Runde ($P(\text{Fortsetzung}|t) = \delta^t$, typischerweise $\delta \in [0{,}2; 0{,}4]$).

**Verhandlungsregeln:**

1. Alle Ressourcenangebote müssen die Gesamtkapazitätsgrenzen einhalten.
2. Private Informationen dürfen geteilt, aber nicht überprüft werden.
3. Koalitionen zwischen zwei Spielern sind erlaubt, aber nicht bindend.
4. Die Verhandlung endet, wenn alle drei Parteien einer Allokation zustimmen oder nach Ablauf der Maximalrunden.

### Phase 4: Post-Experiment (20 Minuten)

- Erneuter FMS-Fragebogen (Erfassung von VR-Sickness nach dem Experiment)
- UIQ (Usability and Interaction Quality Questionnaire)
- Qualitatives Kurzinterview (5–7 Minuten je Teilnehmer)

## VR-Umgebung

Die VR-Umgebung wurde in Unity entwickelt und zeigt einen stilisierten, aber realistisch wirkenden Konferenzraum. Besonderheiten:

- **Avatare:** Vollkörper-Avatare mit Oberkörper-Tracking; Gestik und Kopfbewegungen werden in Echtzeit übertragen.
- **Räumliches Audio:** Spatial Audio vermittelt die Richtung und Entfernung von Gesprächspartnern.
- **Ressourcen-Interface:** Ein virtuelles Display zeigt die aktuellen Verhandlungsangebote und verbleibenden Ressourcen.
- **Datenschutz:** Keine Aufzeichnung von Biometrie-Rohdaten; alle Bewegungsdaten werden ausschließlich lokal verarbeitet.

## Erhobene Variablen (CIPD)

| Variable | Erfassungsmethode |
|---|---|
| Technische Probleme | Auszählung durch Beobachter |
| Explizite VR-Äußerungen | Qualitative Kodierung (Transkript) |
| Gestikulation / gerichtete Gesten | Verhaltenskodierung (Video-Beobachtung) |
| Verhandlungsrunden bis Einigung | Protokoll |
| Endallokation je Spieler | Protokoll |

## Methodische Hinweise

Die räumliche Trennung der Teilnehmer in drei separate physische Räume ist eine bewusste Designentscheidung: Sie stellt sicher, dass die Verhandlung ausschließlich über VR stattfindet und kein para-verbaler oder nicht-virtueller Kontakt möglich ist. Gleichzeitig simuliert dies realistische geografisch verteilte Kollaboration, wie sie in KMU mit mehreren Standorten üblich ist.

Teilnehmer werden ausdrücklich aufgefordert, Unwohlsein oder Symptome von VR-Sickness sofort zu melden. Ein frühzeitiger Abbruch ist jederzeit ohne Konsequenzen möglich.
