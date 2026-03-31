# VR im Mittelstand: Investieren oder abwarten?

**Ein praxisorientierter Leitfaden für mittelständische Unternehmen**
Prof. Dr. Till Albert · Flensburg / Schleswig-Holstein

---

## Über dieses Projekt

Dieses Repository enthält die Materialien für ein laufendes Forschungs- und Transferprojekt zur Nutzung von **Virtual Reality (VR) in kleinen und mittleren Unternehmen (KMU)**, mit besonderem Fokus auf VR-gestützte Meetings und Kollaborationsszenarien im norddeutschen Grenzraum Schleswig-Holstein/Dänemark.

Das Projekt hat über mehrere Jahre hinweg Wissen in verschiedenen Formaten und Aggregationsstufen erzeugt: frühe Gliederungsentwürfe, LaTeX-Kapitel, empirische Feldnotizen, Workshop-Dokumentationen, spieltheoretische Modelle und branchenspezifische Checklisten. Diese heterogenen Fragmente werden nun in ein einheitliches, veröffentlichungsfähiges Handbuch überführt.

---

## Das Konsolidierungsvorhaben

### Ausgangslage

Das Ausgangsmaterial umfasst:

- **Frühe Konzeptdokumente** (`VR Meetings in KMU.md`) — Gliederungsbegründungen, Meeting-Charakterisierungen, Glossar
- **LaTeX-Kapitel** (ca. 15 `.tex`-Dateien) — Best Practices, Fallstudien, Kosten-Nutzen-Analyse, Branchenpotenziale, Implementierungsstrategien, Risikoanalyse, Zukunftsausblick
- **Framework-Dokument** (`Framework_v2.drawio.svg` + PDF) — das 7-Domänen-Forschungsframework
- **Spieltheorie-Kapitel** (`Game-Theory.tex`) — Prinzipal-Agent-Modell für VR-Verhandlungsszenarien
- **Workshop-Unterlagen** (`Workshops/`) — Szenariodokumentation und Erhebungsinstrumente
- **Feldexperiment-Aufzeichnungen** — LIDAR-Scanning, 360°-Fotografie, VR-Messestand, EEG-Pilotversuch
- **Bibliographie** (`literatur.bib`) — gemeinsame Quelldatenbank

### Ziel

Aus diesen Fragmenten entsteht ein kohärentes **Handbuch** für KMU-Entscheider, das den aktuellen Wissensstand des Projekts systematisch zusammenführt und zugleich als Grundlage für den Zwischenbericht gegenüber dem Fördermittelgeber dient.

### Werkzeug: Claude Code

Die Konsolidierung wird mit **Claude Code** (Anthropic CLI) durchgeführt. Claude Code übernimmt dabei:

- Portierung von LaTeX-Inhalten nach Markdown (verlustfrei, mit Erhalt von Mathematik, Tabellen, Querverweisen)
- Strukturelle Analyse der Fragmentsammlung und Lückenerkennung
- Erstellung und Pflege der `OFFENE_PUNKTE.md` als lebendes Aufgabenregister
- Aufbau einer konsistenten Kapitelstruktur nach dem 7-Domänen-Framework
- Führung eines persistenten Gedächtnisses über Projektentscheidungen (Memory-System)

Dieser Ansatz erlaubt es, einen komplexen, über Jahre gewachsenen Dokumentenkorpus iterativ und nachvollziehbar in eine einheitliche Form zu bringen — ohne dabei Inhalte zu verlieren oder inkonsistente Parallelversionen entstehen zu lassen.

---

## Dokumentstruktur

### Aktives Manuskript: `Buch/`

Das Buchmanuskript wird in **Markdown** verfasst und mit **Quarto + Typst** zu PDF und HTML gerendert. Die LaTeX-Dateien bleiben als Archiv erhalten.

```
Buch/
├── _quarto.yml                           ← Quarto-Konfiguration (Typst + HTML)
├── index.md                              ← Vorwort
├── 01_einfuehrung.md                     ← Einführung und Problemstellung
├── 02_framework.md                       ← 7-Domänen-Framework (zentral)
├── 03_betriebswirtschaftlicher_nutzen.md ← Domäne 1: ROI, Kosten-Nutzen
├── 04_anwendungsszenarien.md             ← Domäne 2: Meeting-Typen, Szenarien
├── 05_wissenschaftliche_basis.md         ← Domäne 3: UTAUT, Spieltheorie
├── 06_empirische_untersuchung.md         ← Domäne 4: Workshops, Feldexperimente
├── 07_person_individuum.md               ← Domäne 5: Akzeptanz, VR-Sickness
├── 08_technische_implementation.md       ← Domäne 6: Hardware, DSGVO
├── 09_trends.md                          ← Domäne 7: Zukunftsausblick
├── 10_implementierungsleitfaden.md       ← Assessment, Entscheidungsmatrix
├── Workshop/
│   ├── workshop_szenario.md              ← Verhandlungsszenario (Prinzipal-Agent)
│   └── spieltheorie.md                   ← Spieltheoretisches Modell
└── Anhang/
    ├── A_glossar.md                      ← 37 VR-Begriffe
    ├── B_checklisten.md                  ← Branchenspezifische Checklisten
    ├── C_utaut_fragebogen.md             ← UTAUT-Erhebungsinstrument
    └── D_ressourcen.md                   ← Kuratierte Literatur und Ressourcen
```

### Archiv: LaTeX-Quelldateien

Die ursprünglichen `.tex`-Dateien und `main.tex` verbleiben im Projektverzeichnis als inhaltliches Archiv und Referenz.

---

## Das 7-Domänen-Framework

Das Forschungsframework strukturiert die Analyse von VR in KMU entlang sieben Domänen:

| # | Domäne | Kern |
|---|--------|------|
| 1 | Betriebswirtschaftlicher Nutzen | ROI, Kosten, Wettbewerbsvorteil |
| 2 | VR-Anwendungsszenarien | Meeting-Typen, Branchenszenarien |
| 3 | Wissenschaftliche Basis | UTAUT, Spieltheorie, Forschungsstand |
| 4 | Empirische Untersuchung | Workshops, Feldexperimente, Hypothesen |
| 5 | Person / Individuum | Akzeptanz, Nutzungsbereitschaft, Persönlichkeit |
| 6 | Technische Implementation | Hardware, Software, DSGVO-Compliance |
| 7 | Trends | KI-Integration, Technologieentwicklung |

---

## Empirische Basis

Das Projekt stützt sich auf eigene Feldexperimente:

- **Verhandlungs-Workshop** (Prinzipal-Agent-Szenario in VR)
- **LIDAR-Scanning** mit iPhone 15 Pro (negatives Ergebnis, dokumentiert)
- **360°-Fotografie** für Wert- und Schadensgutachten (Kooperation: sportboot-gutachter.de)
- **VR-Messestand** (Kooperation: Orion, Omnicon Group, Neox Studios, Flensburg)
- **Muse S EEG-Pilotversuch** (abgebrochen, methodisch dokumentiert)
- **Geplant**: KI-Avatar als Verhandlungspartner

---

## Projektstand

Den aktuellen Aufgabenstand, offene Punkte und Priorisierungen enthält:

→ [`OFFENE_PUNKTE.md`](OFFENE_PUNKTE.md)

---

## Technische Voraussetzungen (Rendering)

```bash
# Quarto und Typst müssen installiert sein
quarto render Buch/
```

Ausgabe: PDF (via Typst) und HTML im `_book/`-Verzeichnis.

---

## Kontext

Dieses Vorhaben ist Teil eines **geförderten Forschungs- und Transferprojekts** an der Hochschule Flensburg. Der geografische Schwerpunkt liegt im deutsch-dänischen Grenzraum (Schleswig-Holstein). Die Ergebnisse sollen KMU im Norden bei der Entscheidung über VR-Investitionen unterstützen und einen Beitrag zur anwendungsorientierten VR-Forschung leisten.
