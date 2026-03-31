---
title: "Das Forschungsframework"
---

## Überblick

Das Framework ist das zentrale Ergebnis dieses Forschungsprojekts. Es integriert sieben Domänen, die gemeinsam eine strukturierte Entscheidungsgrundlage für KMU bilden.

## Die sieben Domänen

### 1. Betriebswirtschaftlicher Nutzen

Bewertung von Kosteneinsparungen, Effizienzgewinnen und Umsatzpotenzialen durch VR-Einsatz. Enthält branchenspezifische Kosten-Nutzen-Analysen und ROI-Berechnungen.

### 2. VR-Anwendungsszenarien

Katalog konkreter Einsatzmöglichkeiten nach Branche und Unternehmenstyp, von virtuellen Meetings über Schulungen bis zu Produktpräsentationen.

### 3. Wissenschaftliche Basis

Fundierung des Frameworks durch Akzeptanzmodelle (UTAUT), Präsenzforschung und empirische Studien zur VR-Wirksamkeit.

### 4. Empirische Untersuchung

Eigene experimentelle Studie mit dem Principal-Agent-Paradigma in VR-Meetings, durchgeführt mit BWL-Studierenden.

### 5. Person und Individuum

Individuelle Faktoren wie Technikaffinität (ATI), Erfahrung, Alter und VR-Sickness-Anfälligkeit, die die Eignung für VR-Einsatz beeinflussen.

### 6. Technische Implementation

Hardwareanforderungen, Softwareplattformen, Netzwerkinfrastruktur und Sicherheitsaspekte für den Unternehmenseinsatz.

### 7. Trends und Zukunft

Technologische Entwicklungen, branchenspezifische Trends und Empfehlungen für langfristige VR-Strategien.

## Anwendung des Frameworks

Das Framework wird als Bewertungsinstrument eingesetzt: Jede Domäne liefert einen Score, der in eine Gesamtempfehlung einfließt. Die Gewichtung der Domänen kann je nach Unternehmenskontext angepasst werden.

---

## Beziehungen zwischen den Domänen

Das Framework ist kein lineares Modell. Die Domänen stehen in wechselseitigen Beziehungen, die im SVG-Diagramm durch zwei Kantentypen ausgedrückt werden:

- **„hat"** — hierarchische Eltern-Kind-Beziehung (z. B. BN *hat* ROI als Sub-Knoten)
- **„beeinflusst"** — gerichtete Wechselwirkung zwischen Domänen

Die nachfolgende Tabelle fasst die wichtigsten domänenübergreifenden Abhängigkeiten zusammen. Jede Verbindung ist im jeweiligen Kapitel erklärt.

| Von | → Nach | Beziehung | Erklärung |
|-----|--------|-----------|-----------|
| **BN** (Kap. 03) | **VA** (Kap. 04) | *beeinflusst* | Das Usecase Portfolio (BN) bestimmt, welche Anwendungsszenarien für ein Unternehmen prioritär sind |
| **BN** (Kap. 03) | **P** (Kap. 07) | *hat* | „Individuelle VR Adaptionsfähigkeit" ist Sub-Knoten von BN/Personalressourcen und gleichzeitig Kern von Kap. 07 |
| **BN** (Kap. 03) | **TI** (Kap. 08) | *hat* | Hardware-Infrastruktur und Softwareanforderungen erscheinen als Kostenpositionen in BN und als technische Spezifikationen in TI |
| **BN** (Kap. 03) | **Kap. 10** | *beeinflusst* | Implementierungsempfehlung (BN-Sub-Knoten) leitet direkt zum Implementierungsleitfaden über |
| **VA** (Kap. 04) | **P** (Kap. 07) | *beeinflusst* | VR Adaptionsfähigkeit ist geteilter Knoten: VA bewertet szenariobezogene Eignung, P beschreibt personenbezogene Voraussetzungen |
| **VA** (Kap. 04) | **EU** (Kap. 06) | *beeinflusst* | CIPD-Variablen und Meeting-Partizipant in VA werden im empirischen Workshop operationalisiert |
| **VA** (Kap. 04) | **TI** (Kap. 08) | *hat* | VR Applikation (VA) setzt bestimmte VR-Module und Software (TI) voraus |
| **WB** (Kap. 05) | **EU** (Kap. 06) | *beeinflusst* | Hypothesen (WB) werden im Evaluationsworkshop (EU) getestet; Ergebnisse (EU) fließen zurück als Evaluation (WB) |
| **EU** (Kap. 06) | **WB** (Kap. 05) | *beeinflusst* | Studienergebnisse und Nutzerrückmeldungen (EU) erweitern den Stand der lit. Querverweise (WB) |
| **P** (Kap. 07) | **VA** (Kap. 04) | *beeinflusst* | Individuelle VR-Eignung (P) beeinflusst die erreichbare Wahrgenommene Wirksamkeit (VA) |
| **P** (Kap. 07) | **EU** (Kap. 06) | *beeinflusst* | Studienteilnehmer (EU) werden nach P-Kriterien (ATI, Alter) ausgewählt und charakterisiert |
| **TI** (Kap. 08) | **VA** (Kap. 04) | *beeinflusst* | VR-Module und Software (TI) determinieren den Funktionsumfang realisierter VR-Applikationen (VA) |
| **T** (Kap. 09) | **TI** (Kap. 08) | *beeinflusst* | Technische Trends (T) bestimmen den Entwicklungspfad für VR-Technologie und Hardware (TI) |
| **T** (Kap. 09) | **BN** (Kap. 03) | *beeinflusst* | Wirtschaftliche Trends (T) verändern Wettbewerbsfähigkeits- und ROI-Bewertungen (BN) |
| **T** (Kap. 09) | **VA** (Kap. 04) | *beeinflusst* | Sozio-kulturelle Trends (T) erzeugen neue Meeting-Typen und Anwendungsszenarien (VA) |

## Geteilte Schlüsselkonzepte

Einige Sub-Knoten erscheinen in mehreren Domänen und markieren damit die wichtigsten Verbindungspunkte:

| Konzept | Erscheint in | Bedeutung |
|---------|-------------|-----------|
| **VR Adaptionsfähigkeit** | VA + P | In VA: Eignung eines Szenarios für VR. In P: Individuelle Fähigkeit zur VR-Nutzung. Beide Seiten müssen zusammenpassen. |
| **CIPD-Variablen** | VA + EU | In VA: als Messgröße der Meeting-Qualität definiert. In EU: konkret erhoben im Workshop-Experiment. |
| **Technologieakzeptanz** | EU + WB | In EU: empirisch gemessen (ATI, FMS, UIQ). In WB: theoretisch modelliert (UTAUT). |
| **Hardware-Infrastruktur** | BN + TI | In BN: als Kostenfaktor und Personalressource. In TI: als technische Spezifikation und Implementierungsdetail. |
| **Implementierungsempfehlung** | BN + Kap. 10 | In BN: als erwartetes Ergebnis der Domäne. In Kap. 10: als vollständig ausgearbeiteter Leitfaden. |
