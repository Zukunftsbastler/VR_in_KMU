# PROJEKTSTATUS — VR im Mittelstand
> Stand: 2026-05-05 · Für neue Sessions: Diese Datei zuerst lesen, dann README.md und OFFENE_PUNKTE.md

---

## Wer / Was / Warum

- **Projekt**: Forschungs- und Transferprojekt, gefördert durch **LandSH** (Land Schleswig-Holstein)
- **Autor**: Prof. Dr. Till Albert, Hochschule Flensburg
- **Ziel**: Praxisorientiertes Handbuch für KMU-Entscheider (VR-Investitionsentscheidung) + Zwischenbericht für Fördermittelgeber
- **Geografischer Fokus**: Schleswig-Holstein / deutsch-dänischer Grenzraum — gehört explizit in den Zwischenbericht
- **Software-Tool**: Unity-Applikation existiert bereits → GitHub: https://github.com/phillipja/BeyondRealityResearch

---

## Aktueller Stand des Buchmanuskripts

Das Handbuch liegt in `Buch/` als Markdown-Dateien vor (Quarto + Typst-Rendering). **Alle 19 Dateien existieren.**

```
Buch/
├── _quarto.yml
├── index.md                          ← LEER, noch zu verfassen
├── 01_einfuehrung.md                 ✅ portiert
├── 02_framework.md                   ✅ 7-Domänen-Framework, SVG eingebunden
├── 03_betriebswirtschaftlicher_nutzen.md  ✅
├── 04_anwendungsszenarien.md         ✅ Meeting-Taxonomie, belegte Fallstudien
├── 05_wissenschaftliche_basis.md     ✅ UTAUT, Spieltheorie-Grundlagen
├── 06_empirische_untersuchung.md     ✅ Workshop n=15, aber Feldexperimente fehlen noch
├── 07_person_individuum.md           ✅
├── 08_technische_implementation.md   ⚠️ DSGVO-Analyse Meta Quest fehlt noch
├── 09_trends.md                      ✅
├── 10_implementierungsleitfaden.md   ✅
├── Workshop/
│   ├── workshop_szenario.md          ✅
│   └── spieltheorie.md               ✅ H1–H18, qualitativer Abgleich
├── Anhang/
│   ├── A_glossar.md                  ✅ 37 Begriffe
│   ├── B_checklisten.md              ✅
│   ├── C_messinstrumente.md          ✅ ATI-S, FMS, UEQ-S, CIPD
│   └── D_ressourcen.md               ⚠️ Grundstruktur, vertiefen
└── testcases_coverage.md             ✅ 20 SH-Testfälle
```

---

## Offene Aufgaben nach Priorität

### 🔴 SOFORT — Zwischenbericht-kritisch

| # | Aufgabe | Aktueller Stand | Nächster Schritt |
|---|---------|-----------------|-----------------|
| **S1** | **Zwischenbericht verfassen** (Sachbericht für LandSH) | ⚠️ Struktur vollständig (`Zwischenbericht/`, 6 Abschnittsdateien). Zusammenfassung und AP-Fortschritt ausgearbeitet. Mehrere `<!-- TODO -->` offen: Förderkennzeichen/FKZ, exakte Projektlaufzeit, Datum Workshop, VR-Hardware im Budget, Gründe für Verzögerungen H3, Zeitraum für Gegenmaßnahme in 4.3. | Offene TODOs im Gespräch mit Prof. Albert klären und eintragen, dann Abschnitte zu einem Dokument zusammenführen |
| **S2** | **LIDAR-Negativbefund** in `06_empirische_untersuchung.md` einarbeiten | ⚠️ Vollständiger Entwurf liegt in `Buch/Entwuerfe/H1_lidar_scanning.md` vor (inkl. Gaussian Splatting Ausblick, Handlungsempfehlungen). **Noch nicht** in `06_empirische_untersuchung.md` eingefügt. | Copy-in: Abschnitt nach „Verhaltensbeobachtung" in `06_empirische_untersuchung.md` einfügen |
| **S3** | **360°-Fotografie-Fallstudie** (Stefan Bruns, sportboot-gutachter.de) | ⚠️ Entwurf in `Buch/Entwuerfe/S3_360grad_fotografie_fallstudie.md`: Technische Umsetzung (Skybox, POI, Navigation) beschrieben. Offene Punkte: Einverständnis Stefan Bruns, Anzahl Aufnahmepositionen, Nutzertestergebnisse, eingesetzte VR-Hardware, Bewertung Praxispartner. Noch nicht in `06_empirische_untersuchung.md` integriert. | Rücksprache Stefan Bruns → offene Infos einholen → Entwurf finalisieren → einarbeiten |
| **S4** | **VR-Messestand-Fallstudie** (Orion / Omnicon Group / Neox Studios) | 🔴 Nur Skelett in `Buch/Entwuerfe/S4_vr_messestand_fallstudie.md`. Zielsetzung, Aufbau, Beobachtungen und Ergebnisse sind `<!-- TODO -->`-Platzhalter. Kein einziger inhaltlicher Abschnitt fertig. Im Zwischenbericht als „laufend" vermerkt. | Partner-Einverständnis klären, Details zum Experiment liefern, dann Entwurf befüllen |
| **S5** | **Meta Quest DSGVO-Analyse** → `08_technische_implementation.md` | ⚠️ Generischer Datenschutzabschnitt in `08` vorhanden (ab „Sicherheits- und Datenschutzaspekte in VR"). Keine Meta-Quest-spezifische DSGVO-Analyse. Im Zwischenbericht (4.5) explizit als ausstehend dokumentiert; konzeptionelle Einschätzung (Meta Quest nicht empfehlenswert) bereits vermerkt. | Vollständiges Unterkapitel verfassen: biometrische Daten, Meta-Datenweitergabe, ULD SH als Aufsichtsbehörde, DSGVO-konforme Alternativen (Varjo, HTC Vive) |

### 🟡 KURZFRISTIG (Wochen)

| # | Aufgabe | Benötigte Infos |
|---|---------|----------------|
| **K1** | **Vorwort** (`index.md`) verfassen | Ton (persönlich/akademisch)? Förderung erwähnen? Zielgruppe direkt ansprechen? |
| **K2** | **Muse S EEG-Negativbefund** → `06_empirische_untersuchung.md` | Keine — Begründung in OFFENE_PUNKTE.md H4 vollständig |
| **K3** | **DSGVO-konforme VR-Hardware-Alternativen** (Varjo, HTC Vive etc.) | Tabelle oder Entscheidungsbaum-Grafik? |
| **K4** | **ULD Schleswig-Holstein** als Aufsichtsbehörde referenzieren | ULD-Stellungnahme zu VR-Biometrik bekannt? |
| **K5** | **Testfall-Deckungslücken** schließen (🔴 aus `testcases_coverage.md`) | Sollen alle kritischen Lücken in einem Durchgang adressiert werden? |
| **K6** | **Spieltheorie → Ergebnisse** quantitativ verbinden | Unity-Rohdaten (Allokationen aus Spielclient) verfügbar? |
| **K7** | **Hypothesen-Zuordnung** (PDF S. 19–20) abgleichen | Framework_v2 PDF direkt einsehbar? |

### 🟢 MITTELFRISTIG (Monate)

| # | Aufgabe | Benötigte Infos |
|---|---------|----------------|
| **M1** | **KI-Avatar-Experiment** (nächster Workshop) planen | Zeitplan? Welche KI-API für den Avatar? |
| **M2** | **Quellenabgleich** PDF (12 Einträge) ↔ `literatur.bib` | 5 fehlende Quellen beschaffen: Awa (2015), Elia (2021), Wohlgenannt (2020), Flavián (2019), Radianti (2020) |
| **M3** | **Quarto + Typst Rendering** testen (SVG-Pfad, `quarto render Buch/`) | Quarto + Typst installiert? |
| **M4** | **Anhang D_ressourcen.md** vertiefen (SH-Förderprogramme: WTSH, IB.SH, Interreg?) | Bekannte Programme? |
| **M5** | **Quelle [6]** (Çolak & Yılmaz, 2022) im LaTeX-Archiv bereinigen | Nur LaTeX-Archiv, niedrige Priorität |

---

## Bereits abgeschlossene Arbeitspakete (seit März/April 2026)

- ✅ Komplette `Buch/`-Struktur aufgebaut (Markdown, Quarto/Typst)
- ✅ Alle LaTeX-Inhalte portiert
- ✅ Fiktive Fallstudien entfernt, durch belegte Fälle ersetzt (16 Fälle bereinigt)
- ✅ Meeting-Taxonomie mit 8 Dimensionen und VR-Eignungsbewertung (★–★★★★★)
- ✅ Hypothesenkatalog H1–H18 erstellt (multidisziplinär, mit Literaturbelegen)
- ✅ Messinstrumente dokumentiert (ATI-S, FMS, UEQ-S, CIPD — UTAUT als Referenz behalten)
- ✅ Qualitative Inhaltsanalyse: 102 codierte Aussagen, 6 Kategorien (n=15)
- ✅ `literatur.bib` um peer-reviewed Studien zu VR-Verhandlungen ergänzt
- ✅ 20 SH-Testfälle mit Deckungsanalyse erstellt
- ✅ Zwischenbericht-Struktur aufgebaut (`Zwischenbericht/`, 6 Abschnittsdateien, Hauptinhalte verfasst)
- ✅ LIDAR-Entwurf fertiggestellt (`Buch/Entwuerfe/H1_lidar_scanning.md`, inkl. Gaussian Splatting Ausblick)
- ✅ 360°-Fotografie-Entwurf angelegt (`Buch/Entwuerfe/S3_360grad_fotografie_fallstudie.md`, Technikteil beschrieben)
- ✅ VR-Messestand-Entwurf als Skelett angelegt (`Buch/Entwuerfe/S4_vr_messestand_fallstudie.md`)

---

## Wichtige konzeptionelle Entscheidungen

| Thema | Entscheidung |
|-------|-------------|
| Leitfaden vs. Framework | Leitfaden nutzt Framework als strukturgebenden Unterbau; Experimente zeigen Forschungslücke (keine kommerziellen Anwendungen verfügbar) |
| Geografischer Fokus | LandSH-finanziert → SH-Region ist Kernthema, gehört in Zwischenbericht |
| Nächste Workshops | KI-Avatar als Verhandlungspartner (CEO-Ersatz) geplant |
| Messinstrumente | ATI-S, FMS, UEQ-S statt UTAUT (bessere Antwortquote, aber eingeschränkte Technologieakzeptanzprognose) |
| Meta Quest | Für vertrauliche/personenbezogene Kontexte datenschutzrechtlich nicht empfehlenswert |

---

## Empfohlene Reihenfolge für neue Sessions

1. S1 + S2/S3/S4 parallel: Zwischenbericht-Struktur klären und Feldexperimente einarbeiten
2. S5 + K1: DSGVO-Analyse + Vorwort (in sich abgeschlossen, schnell erledigt)
3. K2–K5: Inhaltliche Vertiefung
4. M1–M5: Qualitätssicherung und geplante Experimente