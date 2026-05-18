# PROJEKTSTATUS — VR im Mittelstand
> Stand: 2026-05-18 · Für neue Sessions: Diese Datei zuerst lesen, dann README.md und OFFENE_PUNKTE.md

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
| **S1** | **Zwischenbericht verfassen** (Sachbericht für LandSH) | ⚠️ **Nahezu fertig** — alle 6 Abschnittsdateien vollständig ausformuliert. Einziger offener Punkt: **Förderkennzeichen (FKZ)** in `01_basisdaten.md` (aus Förderbescheid, muss Prof. Albert liefern). Alle anderen TODOs wurden inzwischen befüllt (Laufzeit, Workshop-Datum, Hardware). | FKZ von Prof. Albert einholen → eintragen → Abschnitte zu einem Abgabedokument zusammenführen |
| **S2** | **LIDAR-Negativbefund** in `06_empirische_untersuchung.md` einarbeiten | ⚠️ Vollständiger Entwurf liegt in `Buch/Entwuerfe/H1_lidar_scanning.md` vor (inkl. Gaussian Splatting Ausblick, Handlungsempfehlungen). **Noch nicht** in `06_empirische_untersuchung.md` eingefügt. | Copy-in: Abschnitt nach „Verhaltensbeobachtung" in `06_empirische_untersuchung.md` einfügen |
| **S3** | **360°-Fotografie-Fallstudie** (Stefan Bruns, sportboot-gutachter.de) — *Experiment aus Vorgängerprojekt, Ergebnisse für dieses Projekt verwertbar* | ⚠️ Entwurf in `Buch/Entwuerfe/S3_360grad_fotografie_fallstudie.md`: Technische Umsetzung (Skybox, POI, Navigation) beschrieben. Offene Punkte: Einverständnis Stefan Bruns, Anzahl Aufnahmepositionen, Nutzertestergebnisse, eingesetzte VR-Hardware, Bewertung Praxispartner. Noch nicht in `06_empirische_untersuchung.md` integriert. | Rücksprache Stefan Bruns → offene Infos einholen → Entwurf finalisieren → als übertragener Befund aus Vorgängerprojekt einarbeiten |
| **S4** | **VR-Messestand-Fallstudie** (Orion / Omnicon Group / Neox Studios) — *Experiment aus Vorgängerprojekt, Ergebnisse für dieses Projekt verwertbar* | ⚠️ **Gestenperzeptionstest vollständig dokumentiert** (`Buch/Entwuerfe/S4_vr_messestand_fallstudie.md`): Protokoll (2 Runden, Distanzvergleich ~2,5 m vs. ~6,5 m, Moderator-Rollenwechsel) beschrieben; empirische Daten eingetragen (N=12, 45 Gesten, **0 % Fehlerquote**). Offen: Messe-Hauptszenario (Zielsetzung, Aufbau der Halle, Produktpräsentation, Navigation, Hauptergebnisse) sowie Partner-Einverständnis und distanzweise Fehlerquoten-Aufschlüsselung. **Nicht** im Zwischenbericht dieses Projekts enthalten, da dem Vorgängerprojekt zuzurechnen. | Partner-Einverständnis klären → Messe-Hauptszenario befüllen (Details von Prof. Albert/Partnern einholen) → distanzweise Fehlerquote nachpflegen |
| **S5** | **Meta Quest DSGVO-Analyse** → `08_technische_implementation.md` | ⚠️ Generischer Datenschutzabschnitt in `08` vorhanden (ab „Sicherheits- und Datenschutzaspekte in VR"). Keine Meta-Quest-spezifische DSGVO-Analyse. Im Zwischenbericht (4.5) explizit als ausstehend dokumentiert; konzeptionelle Einschätzung (Meta Quest nicht empfehlenswert) bereits vermerkt. | Vollständiges Unterkapitel verfassen: biometrische Daten, Meta-Datenweitergabe, ULD SH als Aufsichtsbehörde, DSGVO-konforme Alternativen (Varjo, HTC Vive) |

### 🟡 KURZFRISTIG (Wochen)

| # | Aufgabe | Benötigte Infos |
|---|---------|----------------|
| **K1** | **Vorwort** (`index.md`) verfassen | Ton (persönlich/akademisch)? Förderung erwähnen? Zielgruppe direkt ansprechen? |
| **K2** | **Muse S EEG-Negativbefund** → `06_empirische_untersuchung.md` | ⚠️ Entwurf liegt in `Buch/Entwuerfe/K2_muse_s_eeg_negativbefund.md` vor (Methodenreflexion: Ausgangsfrage, Drei-Ebenen-Bewertung, Handlungsempfehlung, Wearable-Ausblick inkl. Eye-Tracking). **Noch nicht** in `06_empirische_untersuchung.md` eingefügt. → Copy-in: nach „Verhaltensbeobachtung (CIPD-Kodierung)" einfügen |
| **K3** | **DSGVO-konforme VR-Hardware-Alternativen** (Varjo, HTC Vive etc.) | Tabelle oder Entscheidungsbaum-Grafik? |
| **K4** | **ULD Schleswig-Holstein** als Aufsichtsbehörde referenzieren | ULD-Stellungnahme zu VR-Biometrik bekannt? |
| **K5** | **Testfall-Deckungslücken** schließen (🔴 aus `testcases_coverage.md`) | ⚠️ Vier kritische Lücken, unterschiedlicher Status: **(1) Meta Quest DSGVO** → S5; **(2) Berufsgeheimnisschutz** (F08, F13, F18) → Entwurf fertig: `Buch/Entwuerfe/K5_berufsgeheimnisschutz.md` ✅; **(3) Eigene Feldexperimente** (F03, F07) → S2/S3/S4; **(4) Betriebsrat §87 BetrVG** (F14) → Entwurf fertig: `Buch/Entwuerfe/K5_betriebsrat.md` ✅. **Klarstellung:** Punkte (2) und (4) sind nicht VR-spezifisch. Berufsgeheimnisschutz betrifft die Plattformwahl (Meta mit Datenverwertungsgeschäftsmodell vs. neutrale Infrastruktur) — löst sich durch dieselbe Plattformentscheidung wie S5. §87 BetrVG gilt wie für jeden Firmenlaptop und greift nur bei aktiven Monitoring-Features (Eye-Tracking, Aufzeichnung, Produktivitätsmetriken), nicht beim Einsatz als reines Collaboration-Tool. Beide Entwürfe sind als kurze Einschübe formuliert, keine eigenständigen Rechtskapitel. |
| **K6** | **Spieltheorie → Ergebnisse** quantitativ verbinden | ⚠️ **Klarstellung:** Qualitative Auswertung bereits vollständig in `spieltheorie.md` Abschnitt 3.10 (H1/H2 partiell, H4/H9/H10/H14/H16–H18 klar bestätigt). Allokationsrohdaten aus Unity sind nicht für Publikation freigegeben; quantitative Prüfung der allokationsbezogenen Hypothesen (H1, H7) ist damit im aktuellen Projektrahmen nicht möglich. **Drei Alternativen — empfohlen ist (A):** **(A)** Workshop explizit als explorative Pilotstudie rahmen: qualitative Evidenz ist wissenschaftlich ausreichend; quantitative Prüfung als Aufgabe der Folgestudie (→ M1 KI-Avatar-Workshop) benennen — Formulierung „ausstehend" in Abschnitt 3.10 entsprechend ersetzen. **(B)** Simulationsbasierter Benchmark: Modell aus `spieltheorie.md` rechnerisch durchlaufen, theoretische Gleichgewichtsallokationen als Vergleichsfolie generieren (kein Teilnehmerdatenzugang nötig). **(C)** CIPD-Daten als Proxy: bestehende Beobachtungsmetriken (Gesten, Fragen an Versuchsleitung) als quantitative Indikatoren für einzelne Hypothesen nutzen. |
| **K7** | **Hypothesen-Zuordnung** (PDF S. 19–20) abgleichen | ⚠️ **Klarstellung:** Hypothesenkatalog H1–H18 existiert vollständig in `spieltheorie.md` Abschnitt 3.9 — bezieht sich ausschließlich auf den Principal-Agent-Workshop (nicht auf „VR in KMU" allgemein). Alle 18 Hypothesen sind bereits Framework-Domänen zugeordnet (Spalte „Framework-Domäne" in der Übersichtstabelle). Offener Punkt: Das Framework-Dokument (`Framework_v2`) enthält auf S. 19–20 eigene Hypothesen/Propositionen, die noch nicht mit H1–H18 abgeglichen wurden. Erfordert Einsicht in `Framework_v2.drawio` oder einen PDF-Export davon. **Es fehlt kein Hypothesenkatalog** — es fehlt nur die Überprüfung, ob die Framework-PDF-Hypothesen durch H1–H18 abgedeckt sind oder ob ergänzende Hypothesen (z. B. zu anderen Meeting-Typen) formuliert werden müssen. |

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
- ✅ Zwischenbericht nahezu fertiggestellt (`Zwischenbericht/`, alle 6 Abschnittsdateien vollständig ausformuliert — nur FKZ fehlt noch)
- ✅ LIDAR-Entwurf fertiggestellt (`Buch/Entwuerfe/H1_lidar_scanning.md`, inkl. Gaussian Splatting Ausblick)
- ✅ 360°-Fotografie-Entwurf angelegt (`Buch/Entwuerfe/S3_360grad_fotografie_fallstudie.md`, Technikteil beschrieben) — *Experiment stammt aus Vorgängerprojekt; Ergebnisse werden als übertragener Befund ins Buch integriert*
- ✅ VR-Messestand-Entwurf: Gestenperzeptionstest vollständig dokumentiert (`Buch/Entwuerfe/S4_vr_messestand_fallstudie.md` — N=12, 45 Gesten, 0 % Fehlerquote, Distanzprotokoll ~2,5 m vs. ~6,5 m) — *Messe-Hauptszenario noch offen; Experiment stammt aus Vorgängerprojekt*
- ✅ Berufsgeheimnisschutz-Einschub verfasst (`Buch/Entwuerfe/K5_berufsgeheimnisschutz.md`) — für Kap. 08; klärt: nicht VR-spezifisch, betrifft Plattformwahl (Meta vs. neutraler Anbieter)
- ✅ Betriebsrat / §87 BetrVG-Einschub verfasst (`Buch/Entwuerfe/K5_betriebsrat.md`) — für Kap. 10; klärt: greift nur bei aktiven Monitoring-Features, nicht bei Standard-Collaboration-Einsatz

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

1. S1 + S2 parallel: Zwischenbericht finalisieren und LIDAR-Befund einarbeiten; S3/S4 separat als Vorgängerprojekt-Transfers ins Buch aufnehmen (nicht in Zwischenbericht)
2. S5 + K1: DSGVO-Analyse + Vorwort (in sich abgeschlossen, schnell erledigt)
3. K2–K5: Inhaltliche Vertiefung
4. M1–M5: Qualitätssicherung und geplante Experimente