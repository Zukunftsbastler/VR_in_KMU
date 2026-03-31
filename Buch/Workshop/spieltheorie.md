---
title: "Spieltheoretisches Modell"
---

## Einleitung

Das Workshop-Szenario basiert auf einem spieltheoretischen Principal-Agent-Modell für Mehrrundenverhandlungen unter asymmetrischer Information. Das Modell formalisiert die Anreizstrukturen der drei Verhandlungsparteien und erlaubt sowohl theoretische Vorhersagen über optimale Allokationen als auch empirisch beobachtbare Abweichungen durch strategisches Verhalten.

## Grundlegende Modellstruktur

### Basis-Nutzenfunktion

Die Nutzenfunktion für jeden Spieler $i$ ist definiert als:

$$U_i = \prod_{j=1}^{n} x_j^{\alpha_{ij}} + \beta_i\sum_{k=1}^{m} y_k + \gamma_i \theta_i + \lambda_i F_{t+1} + \eta_i E - \sum_{l=1}^{p} \omega_{il}b_l^{\kappa_i}$$

Dabei gilt:

- $x_j$: Primäre Ressourcen (z.B. Budget, Personal, IT-Prioritäten)
- $\alpha_{ij}$: Ressourcen-Gewichtungskoeffizienten (Summe 1 für jeden Spieler)
- $y_k$: Versteckte Ressourcen, die während der Verhandlung entdeckt werden können
- $\beta_i$: Spielerspezifische Gewichtung versteckter Ressourcen
- $\theta_i$: Private Informationskomponente
- $\gamma_i$: Gewichtung privater Informationen
- $F_{t+1}$: Zukunftsorientierte Unternehmensvariablen
- $\lambda_i$: Gewichtung der Zukunftsorientierung
- $E$: Ethische/philanthropische Überlegungen
- $\eta_i$: Gewichtung ethischer Überlegungen
- $b_l$: Negative Güter (Risiken, Umweltauswirkungen, etc.)
- $\omega_{il}$: Spielerspezifische Auswirkung negativer Güter
- $\kappa_i$: Risikoaversionskoeffizient

### Verteilung privater Informationen

Private Informationen folgen einer gemischten Normalverteilung:

$$\theta_i \sim w_i N(\mu_1, \sigma_1^2) + (1-w_i) N(\mu_2, \sigma_2^2)$$

Dabei gilt:

- $w_i$: Mischungsgewicht, nur Spieler $i$ bekannt
- $\mu_1, \mu_2$: Mittelwerte der Komponentenverteilungen
- $\sigma_1^2, \sigma_2^2$: Varianzen der Komponentenverteilungen

### Fortsetzungswahrscheinlichkeit

Die Wahrscheinlichkeit der Fortsetzung nach Runde $t$:

$$P(\text{Fortsetzung}|t) = \delta^t$$

Dabei gilt:

- $\delta$: Diskontierungsfaktor (typischerweise zwischen 0,2 und 0,4)
- $t$: Aktuelle Rundennummer

## Erweiterte Komponenten

### Koalitionsdynamik

Koalitionsbonus zwischen Spielern $i$ und $j$:

$$C_{ij} = \mu_{ij} \min(U_i, U_j)$$

Dabei gilt:

- $\mu_{ij}$: Koalitionsstärke-Koeffizient
- $U_i, U_j$: Individuelle Nutzen der Spieler $i$ und $j$

### Reputationssystem

Reputationsentwicklung über Runden:

$$R_i(t+1) = \delta R_i(t) + (1-\delta)T_i(t)$$

Dabei gilt:

- $R_i(t)$: Reputationswert des Spielers $i$ zum Zeitpunkt $t$
- $T_i(t)$: Vertrauenswürdigkeitsmaß aktueller Handlungen
- $\delta$: Gedächtnisfaktor

### Sigmoid-Nutzenkomponenten

Für Schwellenwerteffekte:

$$S(x) = \frac{L}{1 + e^{-k(x-x_0)}}$$

Dabei gilt:

- $L$: Maximalwert
- $k$: Steilheitsparameter
- $x_0$: Schwellenpunkt

### Leistungsnormalisierung

Individuelle Leistungsnormalisierung:

$$N(U_i) = \frac{U_i}{MaxU_i} \cdot 100\%$$

Unternehmensleistungsmetrik:

$$P_{\text{Unternehmen}} = \sum_{i=1}^{n} w_i N(U_i)$$

Dabei gilt:

- $MaxU_i$: Theoretischer Maximalnutzen für Spieler $i$
- $w_i$: Gewichtung des Beitrags von Spieler $i$ zur Unternehmensleistung
- $N(U_i)$: Normalisierter Nutzen von Spieler $i$

## Konkretes Implementierungsbeispiel

### Nutzenfunktionen der Spieler

#### Forschungsleiterin (Dr. Sarah Chen)

$$U_{\text{Chen}} = (x_1^{0{,}6} \cdot x_2^{0{,}3} \cdot x_3^{0{,}1}) + 0{,}8\sum y_k + 1{,}2\theta_{\text{Chen}} + 0{,}9F_{t+1} + 0{,}2E - 0{,}7(b_1^{1{,}3})$$

Dabei gilt:

- $x_1$: F&E-Budget (in Mio. €)
- $x_2$: Personal (in VZÄ)
- $x_3$: IT-Kapazität (in Servereinheiten)
- $\theta_{\text{Chen}}$: Private Information über Quantencomputing-Fortschritte

Dr. Sarah Chen ist Forschungsleiterin. Ihre Nutzenfunktion legt besonderen Wert auf F&E-Ressourcen und zukünftige Technologieentwicklungen. Ihre private Information bezieht sich auf vielversprechende Forschungsergebnisse im Bereich Quantencomputing.

#### Vertriebsleiter (Marcus Weber)

$$U_{\text{Weber}} = (x_1^{0{,}2} \cdot x_2^{0{,}5} \cdot x_3^{0{,}3}) + 0{,}4\sum y_k + 0{,}8\theta_{\text{Weber}} + 0{,}3F_{t+1} + 0{,}1E - 0{,}4(b_1^{0{,}8})$$

Dabei gilt:

- $\theta_{\text{Weber}}$: Private Information über potenziellen Großauftrag
- Übrige Variablen wie in Chens Nutzenfunktion definiert

Marcus Weber ist Vertriebsleiter. Seine Nutzenfunktion priorisiert kurzfristige Markterfolge. Seine private Information betrifft einen potenziellen Großauftrag.

#### Finanzvorstand (Thomas Bauer)

$$U_{\text{Bauer}} = (x_1^{0{,}3} \cdot x_2^{0{,}4} \cdot x_3^{0{,}3}) + 0{,}6\sum y_k + 0{,}6\theta_{\text{Bauer}} + 0{,}6F_{t+1} + 0{,}3E - 0{,}8(b_1^{1{,}1})$$

Dabei gilt:

- $\theta_{\text{Bauer}}$: Private Information über geplante Regulierungsänderungen
- Übrige Variablen wie in Chens Nutzenfunktion definiert

Thomas Bauer ist Finanzvorstand. Seine Nutzenfunktion balanciert verschiedene Unternehmensinteressen. Seine private Information bezieht sich auf geplante Regulierungsänderungen.

### Ressourcenbeschränkungen

Gesamtverfügbare Ressourcen:

$$\sum x_1 \leq 10 \text{ Mio. €}$$
$$\sum x_2 \leq 50 \text{ VZÄ}$$
$$\sum x_3 \leq 1000 \text{ Servereinheiten}$$

## Ressourcenallokation

### Optimale Allokation unter perfekter Information

Unter perfekter Information und in einer einzelnen Runde wäre die optimale Allokation:

**Dr. Chen:**

- 6 Mio. € (F&E-Fokus)
- 15 VZÄ
- 200 Servereinheiten

**Weber:**

- 2 Mio. €
- 25 VZÄ (Vertriebsfokus)
- 400 Servereinheiten

**Bauer:**

- 2 Mio. €
- 10 VZÄ
- 400 Servereinheiten

Diese Verteilung maximiert den Gesamtnutzen unter Berücksichtigung der individuellen Prioritäten und würde einen Gesamtnutzenwert von etwa 85% des theoretischen Maximums erreichen.

### Strategische Überlegungen bei mehreren Runden

Ohne perfekte Information und bei mehreren Runden ändert sich die Situation jedoch fundamental. Die Spieler müssen nun:

1. **Ihre privaten Informationen strategisch einsetzen:** Dr. Chen könnte beispielsweise ihre Erkenntnisse zum Quantencomputing zunächst zurückhalten, um in späteren Runden bessere Verhandlungspositionen zu haben.

2. **Koalitionen bilden:** Weber und Chen könnten sich zusammenschließen, um gemeinsam mehr IT-Ressourcen zu erhalten, da beide diese für ihre Ziele benötigen.

3. **Risiken anders bewerten:** Die Möglichkeit weiterer Runden führt zu vorsichtigeren Strategien, da extreme Positionen die Verhandlungsposition in Folgerunden schwächen könnten.

4. **Reputationseffekte berücksichtigen:** Zu aggressive Verhandlungsführung könnte die Kooperationsbereitschaft in späteren Runden reduzieren.

### Realistische Mehrrundenallokation

In der Praxis würde dies zu einer ausgewogeneren Ressourcenverteilung führen:

**Dr. Chen:**

- 4 Mio. €
- 18 VZÄ
- 300 Servereinheiten

**Weber:**

- 3 Mio. €
- 20 VZÄ
- 350 Servereinheiten

**Bauer:**

- 3 Mio. €
- 12 VZÄ
- 350 Servereinheiten

Diese Verteilung erreicht zwar nur etwa 75% des theoretischen Maximums, ist aber unter realistischen Bedingungen stabiler und fördert langfristige Kooperation.

## Bezug zur empirischen Untersuchung

Das spieltheoretische Modell dient als Benchmark für die Auswertung der Workshop-Ergebnisse. Konkret werden folgende Vergleiche angestellt:

- **Vergleich der Endallokation** mit der theoretisch optimalen Allokation unter vollständiger Information
- **Vergleich mit der realistischen Mehrrundenallokation** als Referenzpunkt für strategisches Verhalten
- **Analyse der Reihenfolge von Informationsoffenbarungen** im Verhältnis zur Nutzenfunktion der offenbarenden Partei
- **Überprüfung von Koalitionsbildungen:** Entsprechen die beobachteten Allianzen den durch $C_{ij}$ vorhergesagten Kooperationsanreizen?

Die CIPD-Variablen (technische Probleme, explizite VR-Äußerungen, Gestikulation) liefern ergänzende Informationen darüber, wie die VR-Umgebung selbst das Verhandlungsverhalten beeinflusst – unabhängig von der spieltheoretischen Vorhersage.
