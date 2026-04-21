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

---

## Spieltheoretische Einordnung des implementierten Experiment-Designs

> *Das formale Modell in den vorangehenden Abschnitten beschreibt den ersten Modellierungsstand (Cobb-Douglas-Nutzenfunktionen, drei benannte Rollen). Das tatsächlich implementierte Experiment wurde gegenüber diesem Entwurf vereinfacht; die vollständige Verfahrensbeschreibung findet sich in `Buch/Workshop/workshop_scenario.md`. Dieser Abschnitt bettet das implementierte Design in die spieltheoretische Literatur ein.*

### Grundstruktur: Mehrpersonen-Prinzipal-Agent-Problem mit asymmetrischer Information

Das Verhandlungsexperiment realisiert strukturell ein **Mehrpersonen-Prinzipal-Agent-Spiel unter asymmetrischer Information und wiederholter Interaktion**. Ausgangspunkt ist die klassische zweigliedrige Prinzipal-Agent-Beziehung: Ein Auftraggeber (Prinzipal) delegiert eine Entscheidungsaufgabe an einen Beauftragten (Agenten), dessen Präferenzen und Handlungen er nicht vollständig beobachten kann [@ross1973economic; @jensen1976theory]. Das vorliegende Design weicht in zwei entscheidenden Dimensionen von diesem Grundmodell ab:

**Erstens** sind zwei Agenten anwesend, die gleichzeitig und unabhängig voneinander Allokationsvorschläge an denselben Prinzipal unterbreiten. **Zweitens** ist der Zeithorizont randomisiert und unbekannt — die Interaktion findet über mehrere Runden statt, deren Anzahl den Teilnehmern nicht im Voraus bekannt ist.

### Adverse Selection und Hidden Agenda

*Adverse selection* bezeichnet Situationen, in denen eine Partei entscheidungsrelevante Informationen besitzt, die für die andere vor der Interaktion nicht beobachtbar sind [@mirrlees1971exploration; @eisenhardt1989agency]. Im Experiment entspricht die Hidden Agenda jedes Agenten seiner unbeobachtbaren Präferenzstruktur über die vier Input-Variablen: Der Prinzipal sieht die vorgeschlagenen Allokationen und die daraus resultierenden Unternehmensoutputs, nicht aber, welche Input-Variablen dem Agenten privaten Nutzen bringen. Jeder Agent ist einer randomisierten Persona mit bis zu drei spezifischen Nutzungszielen zugeordnet (max. 10 Punkte je Ziel), die an bestimmte Input-Variablen gekoppelt sind.

Die klassische *Screening*-Logik [@myerson1979incentive] ist hier invertiert: Nicht der Prinzipal bietet ein Vertragsmenü an, um Agenten zur Selbstselektion zu bewegen, sondern die **Agenten konkurrieren darum, einen Vorschlag zu präsentieren, der für den Prinzipal attraktiv wirkt**, während sie ihre privaten Präferenzen verschleiern. Dies entspricht einem *informed agent, uninformed principal*-Setting.

Beobachtete Verhaltenstendenz: Agenten waren auffallend zurückhaltend gegenüber Fragen zu ihren Nutzungspunkten, aber überraschend offen mit den vorgeschlagenen Input-Werten — häufig unter der irrtümlichen Annahme, der Prinzipal habe bereits Zugang zu diesen Zahlen. Dieses Muster ist konsistent mit *bounded rationality* [@simon1955behavioral]: Teilnehmer modellierten die Informationsstruktur des Spiels unvollständig.

### Wettbewerb zwischen Agenten: Yardstick Competition und Turniermechanismus

Die simultane Anwesenheit zweier konkurrierender Agenten verändert die Anreizstruktur fundamental gegenüber dem zweigliedrigen Modell [@holmstrom1982moral]. Holmström (1982) zeigt, dass ein Prinzipal mit mehreren Agenten relative Leistungsvergleiche als Informationsquelle nutzen kann, um Informationsrenten zu reduzieren. Shleifer (1985) formalisiert diesen Mechanismus als *yardstick competition*: Der Prinzipal bewertet jeden Agenten relativ zum anderen — was im Experiment direkt abgebildet wird, da der Prinzipal beide Vorschläge gleichzeitig auf dem Screen sieht und vergleichend bewertet [@shleifer1985yardstick].

Lazear & Rosen (1981) zeigen mit ihrem Modell der *rank-order tournaments*, dass Rangordnungswettbewerbe unter bestimmten Bedingungen individuell kalibrierte Verträge informationseffizient ersetzen können: Der Prinzipal muss nur den Gewinner ermitteln, nicht die absolute Leistung messen [@lazear1981rank]. Das vorliegende Design enthält eine abgeschwächte Turnierdimension — der Prinzipal genehmigt Vorschläge selektiv, kann aber beide Agenten separat approven oder ablehnen, was das reine Null-Summen-Turnier aufweicht.

Demski & Sappington (1984) zeigen für Multi-Agent-Settings mit unkorrelierten Typen, dass relative Leistungsvergleiche die Informationsrenten der Agenten vollständig eliminieren können [@demski1984optimal]. Da die privaten Nutzungsziele im Experiment per Zufallszuweisung verteilt werden und damit zwischen den Agenten einer Gruppe tatsächlich unkorreliert sind, ist diese theoretische Bedingung näherungsweise erfüllt.

### Strategische Informationsoffenbarung: Cheap Talk

Das Experiment erlaubt Teilnehmern explizit, private Informationen zu teilen, schließt deren Verifizierbarkeit jedoch aus. Dies ist die Grundstruktur des *cheap talk*-Modells von Crawford & Sobel (1982): Kommunikation ist kostenlos, aber nicht bindend und nicht beweisbar [@crawford1982strategic].

Das zentrale Ergebnis von Crawford & Sobel: Informative Kommunikation ist im Gleichgewicht nur möglich, wenn die Interessen von Sender (Agent) und Empfänger (Prinzipal) nicht zu stark divergieren. Bei großer Zieldivergenz wird nur grobe Information übertragen. Da im Experiment die privaten Nutzungsziele der Agenten mit den Unternehmenszielen des Prinzipals kollidieren können, ist zu erwarten, dass rationale Agenten keine vollständige Information preisgeben — was mit der beobachteten Zurückhaltung bezüglich der Punkteziele konsistent ist.

### Wiederholtes Spiel mit unbekanntem Zeithorizont

Ein zentrales Design-Element ist die randomisierte Rundenanzahl: mindestens drei Runden, nach denen die Fortsetzungswahrscheinlichkeit exponentiell sinkt und ab Runde 7 unter 1 % liegt. Dieses Design operationalisiert ein Kernproblem der Theorie wiederholter Spiele.

Das *Folk Theorem* besagt: In unendlich wiederholten Spielen mit hinreichendem Diskontfaktor können nahezu beliebige Gleichgewichtsergebnisse auftreten, da Spieler glaubwürdig mit der Einstellung zukünftiger Kooperation drohen können [@fudenberg1986folk]. Kooperation zwischen Agent und Prinzipal — etwa die glaubwürdige Offenbarung privater Informationen gegen eine günstigere Ressourcenzuteilung — ist damit auch dann rational, wenn sie in einer Einzelrunde nicht optimal wäre.

Der unbekannte Zeithorizont dient dabei einem konkreten Zweck: In endlichen Spielen mit bekanntem Ende löst backward induction jegliche Kooperation auf (*chain store paradox*, Selten 1978). Durch Randomisierung des Enddatums wird dieser Effekt unterdrückt. Kreps, Milgrom, Roberts & Wilson (1982) zeigen, dass bereits geringe Unsicherheit über die Rationalität des Gegenübers ausreicht, um in finiten Spielen kooperative Gleichgewichte aufrechtzuerhalten [@kreps1982rational] — ein Effekt, der durch die stochastische Rundenzahl des vorliegenden Designs begünstigt wird.

Die beobachtete Verhaltensveränderung zwischen frühen und späten Runden (z. B. Gruppe 3: "Ab der 2. Runde waren die Agenten sehr darauf aus, den Zuschlag des Prinzipals zu bekommen") ist konsistent mit dem Aufbau eines Reputationsmechanismus über Runden hinweg.

### Entwurfsentscheidung: Reduzierung der Variablenkorrelation

Der Wechsel vom ursprünglichen Cobb-Douglas-Modell (multiplikative Nutzenfunktionen, $U_i = \prod x_j^{\alpha_{ij}} + ...$) zum implementierten additiven Design mit entkoppelten Nutzungszielen ist eine methodische Entscheidung mit direkten theoretischen Implikationen.

**Das ursprüngliche Modell** erzeugt *strategische Komplementaritäten*: Die Grenznutzen einer Ressource $x_k$ hängen von der Allokation aller anderen Ressourcen ab. Das entspricht realistischen Ressourcenentscheidungen in Unternehmen, führt aber im Experiment zu einem Identifikationsproblem: Aus dem Verhandlungsverhalten lässt sich nicht isolieren, welche Präferenzen für welche Variable handlungsleitend waren, da jede Allokationsentscheidung mehrere Variablen gleichzeitig betrifft.

**Das implementierte Design** mit additiv-separierten Nutzungszielen löst dieses Problem: Jedes private Ziel ist an eine spezifische Variable geknüpft und bewertet unabhängig von den übrigen. Dies entspricht dem Prinzip der *separability* im Mechanismusdesign — in Setups ohne Variableninteraktion lässt sich die Präferenzstruktur eines Agenten aus wiederholtem Verhalten direkt ablesen [@myerson1979incentive].

Aus der Perspektive der experimentellen Wirtschaftsforschung ist diese Vereinfachung als Entscheidung zugunsten von *Kontrollierbarkeit* gegenüber ökologischer Validität zu verstehen [@smith1976experimental; @kagel1995handbook]. Das Experiment zielt auf die Beobachtung strategischer Kommunikations- und Offenbarungsverhalten — ein Forschungsziel, das durch sauber separierte Anreize besser erreichbar ist als durch realitätsnahe, aber analytisch schwer trennbare Nutzungsstrukturen. Die bewusste Inkaufnahme reduzierter Case-Study-Kohärenz folgt gängiger Praxis in Labor-Wirtschaftsexperimenten.

### Zusammenfassung: Theoretische Struktur des Experiments

| Dimension | Spieltheoretisches Konzept | Literatur |
|---|---|---|
| 1 Prinzipal + 2 konkurrierende Agenten | Multi-Agent Principal | @holmstrom1982moral; @demski1984optimal |
| Private Nutzungsziele (Hidden Agenda) | Adverse Selection | @jensen1976theory; @mirrlees1971exploration |
| Prinzipal vergleicht Vorschläge relativ | Yardstick Competition | @shleifer1985yardstick |
| Agenten konkurrieren um Zustimmung | Rank-Order Tournament | @lazear1981rank |
| Nicht verifizierbare Informationsoffenbarung | Cheap Talk | @crawford1982strategic |
| Randomisierter Zeithorizont (mind. 3 Runden) | Repeated Game / Folk Theorem | @fudenberg1986folk; @kreps1982rational |
| Additiv-separierte Nutzungsziele | Separability / Exp. Kontrolle | @smith1976experimental; @kagel1995handbook |
| Zeitdruck (3–5 Min./Runde) | Bounded Rationality | @simon1955behavioral |

---

## Kommunikationsmedium und Verhandlungsverhalten: VR zwischen Präsenz und Distanz

> *Dieser Abschnitt bettet das Experiment in die Forschungsliteratur zu Medienwahl und Verhandlungsverhalten ein. Er ergänzt die spieltheoretische Einordnung um eine kommunikationswissenschaftliche Perspektive und liefert Erklärungsangebote für die beobachteten Verhaltensweisen. Der Abschnitt ist relevant für die Framework-Domänen **VA** (Anwendungsszenarien, Kap. 04) und **WB** (Wissenschaftliche Basis, Kap. 05).*

### Das Kommunikationsmedium als eigenständige Variable

Neben den spieltheoretischen Anreizstrukturen beeinflusst das **Kommunikationsmedium** selbst, wie Verhandlungen verlaufen — unabhängig davon, welche Interessen die Parteien verfolgen. Diese Erkenntnis ist in der Kommunikationsforschung gut belegt, wird aber in spieltheoretischen Modellen klassischerweise nicht modelliert. Für das vorliegende Experiment ist sie zentral: Das "Spiel" wird nicht in einem neutralen Medium gespielt, sondern in einer immersiven VR-Umgebung — und die Frage ist, welche spezifischen Effekte das Medium auf die Verhandlungsdynamik ausübt und ob diese die spieltheoretisch vorhergesagten Muster verstärken oder abschwächen.

### Zwei klassische Rahmentheorien

**Media Richness Theory** [@daft1986organizational]: Kommunikationsmedien unterscheiden sich in ihrer *Informationsreichhaltigkeit* — dem Grad, in dem sie Rückkopplungsschnelligkeit, Hinweisvielfalt (Tone, Gestik, Mimik), Sprache und persönliche Fokussierung ermöglichen. F2F ist das reichhaltigste Medium; Videokonferenz, Telefon und Text folgen in abnehmender Reihe. Die Theorie sagt voraus: Je höher die Ambiguität einer Aufgabe — und Verhandlungen mit divergierenden Interessen sind per Definition hochgradig mehrdeutig — desto notwendiger ist ein reichhaltiges Medium. Unter dieser Logik wäre VR als medium-high einzustufen: reichhaltigere Raumnutzung und Körpersprache als Videokonferenzen, aber mit dem konkreten Experiment-Fehler der Mimikübertragung.

**Social Presence Theory** [@short1976social]: Soziale Präsenz bezeichnet das wahrgenommene Gefühl der *Mitanwesenheit* eines Gegenübers. Medien unterscheiden sich darin, wie stark sie dieses Gefühl erzeugen. Höhere soziale Präsenz macht Interaktion persönlicher, wärmer und weniger transaktional. In Verhandlungssituationen korreliert höhere soziale Präsenz empirisch mit mehr Vertrauen, mehr Rapport und kooperativeren Ergebnissen [@drolet2000rapport].

Beide Theorien prognostizieren ähnlich: Reichhaltigere Medien und höhere soziale Präsenz → kooperativere, integrativere Verhandlungsergebnisse.

### Empirische Befunde entlang des Medienkontinuums

Die Forschungslage bestätigt diesen Rahmen, jedoch mit relevanten Nuancen:

**F2F-Verhandlungen** begünstigen integrative Einigungen (beide Seiten gewinnen) durch Blickkontakt, Rapport-Signale und unmittelbare nonverbale Rückmeldung [@drolet2000rapport]. Dabei wirkt F2F doppelt: Einerseits erhöht es Vertrauen und Kooperationsbereitschaft; andererseits macht es den emotionalen Einsatz — Gesichtsausdruck, Körpersprache, physische Nähe — sichtbar und damit wirksam.

**Videokonferenz** (Zoom, Teams) ist nicht einfach "schwächeres F2F". Bailenson (2021) zeigt, dass die unnatürliche Kombination aus Gesichtsübertragung, fehlendem Raumgefühl und atypischen Blickkontaktsignalen eigene kognitive Belastungen erzeugt ("Zoom Fatigue") — das Medium ist also nicht nur ärmer, sondern in spezifischer Weise anders [@bailenson2021nonverbal].

**Text- und E-Mail-Verhandlungen** zeigen robuste Nachteile in kompetitiven Kontexten: weniger Einigungen, weniger Vertrauen, höhere strategische Täuschungsbereitschaft [@naquin2003online]. Entscheidend ist der Befund, dass selbst bei gleichem Verhandlungsergebnis die Prozesskvalität schlechter bewertet wird — Misstrauen entsteht unabhängig vom Inhalt, allein durch das Medium.

Moser et al. (2020) zeigen im direkten Vergleich VR vs. Videokonferenz vs. F2F, dass VR für kollaborative Entscheidungsaufgaben in einigen Outcomes zwischen F2F und Video liegt, in anderen jedoch eigenständige Merkmale aufweist, die sich nicht linear auf dem Medienkontinuum verorten lassen [@moser2020vr]. VR ist kein "stärkeres Videomeeting", sondern ein qualitativ anderes Kommunikationsformat.

### Die einzigartige Position von VR: Räumliche Präsenz ohne vollständige Mimikübertragung

VR kombiniert Eigenschaften, die bisher kein Medium gleichzeitig bot: **räumliche Ko-Präsenz und Körperbewegungsübertragung** (höher als in Videokonferenzen) bei **gleichzeitigem Fehlen von Gesichts- und Mimikausdruck** (im vorliegenden Experiment: Roboter-Avatare ohne Gesichtsanimation). Diese Kombination ist theoretisch einzigartig:

| Dimension | Telefon | Video | VR (Experiment) | F2F |
|---|---|---|---|---|
| Räumliche Ko-Präsenz | — | — | ✓ | ✓ |
| Gestik / Körperbewegung | — | eingeschränkt | ✓ (Oberkörper) | ✓ |
| Mimik / Gesichtsausdruck | — | ✓ | ✗ | ✓ |
| Blickkontakt (Avatar) | — | ✗ (Kameraversatz) | ✓ | ✓ |
| Soziale Präsenz | niedrig | mittel | hoch | sehr hoch |

Für Verhandlungssituationen ist das Gesicht der primäre Kanal für Vertrauensbewertung und Täuschungserkennung [@drolet2000rapport]. Räumliche Körpersprache kann Absichten signalisieren, ist aber schwerer zu lesen und leichter zu kontrollieren. Das Experiment setzt Teilnehmer in eine Situation hoher emotionaler Involvierung (Immersion, Wettbewerb) bei gleichzeitig reduzierter Fähigkeit, den Gegenspieler emotional zu *lesen*: Sie fühlen, dass jemand da ist — aber sie können nicht erkennen, was dieser denkt oder empfindet.

Kock (2005) argumentiert in seiner *Media Naturalness Theory*, dass jede Abweichung vom evolutionär "natürlichen" F2F-Kommunikationsmodus kognitiven Mehraufwand erzeugt — Teilnehmer müssen aktiv kompensieren [@kock2005media]. Im vorliegenden Experiment bedeutet das: Die hohe räumliche Präsenz erzeugt Erwartungen, die die fehlende Mimikübertragung systematisch enttäuscht. Dieser Kompensationsaufwand tritt *zusätzlich* zur kognitiven Belastung durch das Spielszenario auf.

### Zwei Hypothesen: Abschwächung oder Verstärkung kompetitiver Dynamik?

Die zentrale theoretische Frage für das Experiment ist, wie sich VR im **kompetitiven** Kontext verhält — ob die Effekte des Mediums und die spieltheoretischen Anreize sich gegenseitig abschwächen oder verstärken:

**Abschwächungs-Hypothese** (VR → kooperativer als reine Videokonferenz):  
Höhere soziale Präsenz → mehr Rapport → Kooperationsbereitschaft steigt; räumliches Einander-Gegenübertreten aktiviert soziale Hemmungen gegenüber zu aggressivem Wettbewerb, ähnlich F2F.

**Verstärkungs-Hypothese** (VR → intensivere Wettbewerbsdynamik als Video):  
Höhere Immersion → stärkerer emotionaler Arousal → kompetitive Anreize werden intensiver erlebt; fehlende Mimikübertragung → Empathiesignale fehlen, die in F2F kooperatives Verhalten moderieren würden; Neuheitseffekt und kognitiver Mehraufwand erzeugen reaktiveres Verhalten, das der dominanten Situationsnorm folgt.

Die Verstärkungs-Hypothese wird durch die **SIDE-Theorie** (Social Identity model of Deindividuation Effects, @postmes1998side) gestützt: Wenn persönliche Identitätssignale reduziert werden — wie durch Roboter-Avatare — verschiebt sich das Verhalten in Richtung der jeweils salientesten sozialen Norm. In einem explizit als Wettbewerb gestalteten Setting (Scoring, kompetitive Rollen) ist die Wettbewerbsnorm hochgradig salient. Deindividuierung durch Avatare verstärkt dann nicht Kooperation, sondern Konformität mit der vorherrschenden Situation: hier Wettbewerb.

### Beobachtungen im Licht der Theorie

Die empirischen Beobachtungen aus dem Experiment sind überwiegend mit der **Verstärkungs-Hypothese** konsistent:

- **Qualitative Kategorie Immersion** (n=29, 28% aller Aussagen): Vergessen der realen Umgebung, motorische Impulse, erhöhtes Stressniveau in der Agentenrolle — konsistent mit erhöhtem emotionalem Arousal
- **Verhaltensbeobachtung:** "Hitzig diskutiert" ab Runde 3 (Gruppe 1); intensive Argumen­tationsarbeit; Wettbewerbsorientierung wächst über Runden (Gruppe 3)
- **Qualitative Kategorie Soziale Präsenz** (n=20): Gefühl des gemeinsamen Raums als stärker als Zoom bewertet — erhöhte soziale Präsenz bestätigt; gleichzeitig: fehlende Mimik als explizit kritisierter Mangel

Dabei ist die Kombination theoretisch aufschlussreich: Die Teilnehmer *berichten* erhöhte soziale Präsenz (was die Abschwächungs-Hypothese stützen würde) — zeigen aber *behavioral* verstärkte Wettbewerbsdynamik. Dies deutet darauf hin, dass im vorliegenden Design die strukturellen Verstärkungseffekte (SIDE-Konformität mit Wettbewerbsnorm, emotionaler Arousal, fehlende Mimik-Moderation) die kooperationsförderlichen Social-Presence-Effekte überwogen.

Diese Interaktion lässt sich als **kontextspezifische Modulationshypothese** formulieren: **VR ist kein universeller Kooperations- oder Wettbewerbsverstärker, sondern ein Immersionsverstärker — er amplifiziert die dominante Valenz des Szenarios.** In einem kooperativen Kontext würde dieselbe VR-Umgebung voraussichtlich Kooperation verstärken; im kompetitiv-incentivisierten Prinzipal-Agenten-Szenario verstärkt sie den Wettbewerb.

### Implikationen für die Framework-Domänen

**→ VA (Kap. 04 — VR-Anwendungsszenarien):** Die Szenario-Eignung für VR ist nicht nur eine Funktion von Aufgabenkomplexität und technischer Machbarkeit, sondern auch des Interaktionstyps. Die hier entwickelte Modulationshypothese gibt eine differenziertere Empfehlung:

| Meeting-Typ | Erwarteter VR-Effekt | Empfehlung |
|---|---|---|
| Kollaborative Problemlösung | Verstärkte Kooperation, höheres Engagement | Geeignet; Vorteil gg. Video |
| Strategische Verhandlung (kompetitiv) | Verstärkte Wettbewerbsdynamik, erhöhter emotionaler Einsatz | Geeignet für Training; in realen Verhandlungen mit Bedacht |
| Sensible Personalgespräche | Fehlende Mimik-Moderation erhöht Missverständnisrisiko | Eingeschränkt geeignet; F2F bevorzugen |
| Statusbehaftete Entscheidungsmeetings | Räumliche Hierarchie (Sitzordnung) wird stärker wahrgenommen als in Video | Geeignet bei klarem Hierarchiekontext |

**→ WB (Kap. 05 — Wissenschaftliche Basis):** Media Richness Theory [@daft1986organizational] und Social Presence Theory [@short1976social] bilden die theoretische Brücke zwischen VR-Forschung und Verhandlungsforschung. Sie begründen, warum VR-spezifische Ergebnisse nicht einfach auf F2F- oder Videokonferenz-Studien extrapolierbar sind. Die kontextspezifische Modulationshypothese ist eine direkte Erweiterung dieser Literatur mit Blick auf kompetitive Interaktionsstrukturen.
