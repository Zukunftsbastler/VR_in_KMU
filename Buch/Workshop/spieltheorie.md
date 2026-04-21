# **3. Spieltheoretische Modellierung eines dynamischen Principal-Agent-Szenarios**

## **3.1 Einleitung**

Das in dieser Arbeit entwickelte Workshop-Szenario modelliert eine dynamische Mehrrundenverhandlung unter asymmetrischer Information auf Basis des Principal-Agent-Ansatzes. Im Zentrum steht die Interaktion zwischen drei Akteuren: einem Principal (CEO) sowie zwei Agenten (Manager A und Manager B).

Jeder Akteur erhält zu Beginn des Szenarios eine zufällig ausgewählte Persona, welche individuelle Präferenzen und Zielsetzungen definiert. Diese Präferenzen sind privat und für die jeweils anderen Akteure nicht beobachtbar, wodurch eine klassische Informationsasymmetrie entsteht.

Das Szenario umfasst mindestens drei Verhandlungsrunden mit einer maximalen Dauer von jeweils fünf Minuten. Die tatsächliche Anzahl der Runden ist jedoch stochastisch und den Akteuren ex ante unbekannt. Diese Unsicherheit verhindert endrundenbasierte Strategien und erhöht die strategische Komplexität.

Im Mittelpunkt jeder Runde steht die Allokation eines Budgets auf vier Stellungsgrößen. Diese beeinflussen sowohl die Entwicklung des Unternehmens als auch die privaten Nutzen der Agenten über nichtlineare und für die Akteure intransparente Zusammenhänge. Dadurch entsteht ein komplexes Entscheidungsumfeld mit konfligierenden Zielsystemen.

---

## **3.2 Modellbeschreibung**

### **3.2.1 Akteure und Rollen**

**Principal (CEO).**  
Der Principal ist primär an der Entwicklung des Unternehmens interessiert, trifft jedoch seine Entscheidungen unter Berücksichtigung einer durch die Persona vorgegebenen Präferenzstruktur. Diese Präferenz kann eine der Dimensionen der Unternehmensperformance besonders gewichten. Eine explizite formale Nutzenfunktion des Principals wird nicht modelliert; stattdessen erfolgt die Entscheidungsfindung im Sinne eines rollenbasierten Verhaltens (Role-Playing).

**Agenten (Manager A und B).**  
Die Agenten maximieren ihren privaten Nutzen, der durch ihre jeweilige Persona definiert ist. Gleichzeitig müssen sie Budgetallokationen vorschlagen, die eine hinreichend hohe Wahrscheinlichkeit besitzen, vom Principal akzeptiert zu werden. Daraus ergibt sich ein Zielkonflikt zwischen individueller Nutzenmaximierung und organisationaler Effizienz.

**Personas.**  
Personas determinieren die Präferenzen der Akteure. Während die Persona des Principals eine implizite Gewichtung der Unternehmensziele vorgibt, definieren die Personas der Agenten deren private Nutzenfunktionen.

---

### **3.2.2 Budget und Entscheidungsraum**

Zu Beginn jeder Runde $t \in \mathbb{N}$ steht ein Budget $b_t > 0$ zur Verfügung, wobei für die erste Runde gilt:

$$b_1 = 15$$

Die Agenten verteilen das Budget auf vier Stellungsgrößen $s_{k,t} \in [0,1]$ mit $k = 1, \dots, 4$. Die Gesamtallokation ist beschränkt durch:

$$\sum_{k=1}^{4} s_{k,t} \leq \frac{4}{3}$$

Das verbleibende Budget nach Allokation ergibt sich zu:

$$b_t^{res} = b_t \left(1 - \frac{1}{3} \sum_{k=1}^{4} s_{k,t} \right)$$

Diese Formulierung erlaubt eine Überallokation des Budgets bis zu 133 %, was zur Aufnahme von Schulden führt.

---

### **Verschuldung**

Im Falle einer Überallokation ($b_t^{res} < 0$) wird ein Kredit mit einem Zinssatz von 100 % aufgenommen. Das effektive Budget ergibt sich somit zu:

$$b_t^{final} = \begin{cases} b_t^{res}, & \text{falls } b_t^{res} \geq 0 \\ 2 \cdot b_t^{res}, & \text{falls } b_t^{res} < 0 \end{cases}$$

---

### **3.2.3 Spielende**

Das Spiel endet entweder durch Insolvenz ($b_t^{final} < 0$) oder durch ein stochastisches Abbruchkriterium ab Runde $t \geq 3$.

Die Fortsetzungswahrscheinlichkeit ist definiert als:

$$P(\text{Fortsetzung in Runde } t) = \begin{cases} 1, & t < 3 \\ \frac{1}{t - 2}, & t \geq 3 \end{cases}$$

Diese Konstruktion impliziert eine mit zunehmender Rundenzahl sinkende Fortsetzungswahrscheinlichkeit.

---

## **3.3 Unternehmensdynamik**

Die Entwicklung des Unternehmens wird durch vier zentrale Outputgrößen bestimmt:

- Direkter Umsatz $u_t$
- Zukünftige Investitionen $i_t$
- Sozialpolitische Sichtbarkeit $s_t$
- Ethisches Verhalten $e_t$

Das Budget der folgenden Runde ergibt sich zu:

$$b_{t+1} = b_t^{final} + i_{t-1} \cdot u_t + \mathbb{1}_{\{x_t < s_t\}} \cdot e_t \cdot 10 \cdot t^2$$

mit einer Zufallsvariable:

$$x_t \sim \mathcal{U}(0,1)$$

Für die Initialisierung gilt:

$$i_0 = 1$$

Die sozialpolitische Sichtbarkeit $s_t$ bestimmt die Eintrittswahrscheinlichkeit eines externen Ereignisses, dessen Wirkung durch das ethische Verhalten $e_t$ moduliert wird.

---

### **3.3.1 Funktionale Zusammenhänge**

Die Outputgrößen basieren auf transformierten Stellungsgrößen:

$$\tilde{s}_{k,t} = e_k(s_{k,t})$$

Die Transformationsfunktionen werden in jeder Runde zufällig zugewiesen und sind den Akteuren nicht bekannt.

**Transformationsfunktionen:**

- Linear:

$$f(x) = a x, \quad a \in (0,1)$$

- Stufenfunktion:

$$g(x) = \begin{cases} 0, & x < 0{,}33 \\ 0{,}5, & 0{,}33 \leq x < 0{,}66 \\ 1, & x \geq 0{,}66 \end{cases}$$

- Ease-In-Out:

$$h(x) = \begin{cases} 2x^2, & x < 0{,}5 \\ 1 - \dfrac{(-2x + 2)^2}{2}, & x \geq 0{,}5 \end{cases}$$

- Sinusfunktion:

$$i(x) = 0{,}5 + \frac{1}{4} \left[ \sin\!\left(\frac{3\pi}{2} + 2\pi x\right) + \sin\!\left(\frac{3\pi}{2} + 5\pi x\right) \right]$$

---

Die aggregierte Wirkung auf eine Unternehmensvariable $j \in \{u,i,s,e\}$ ergibt sich zu:

$$S_{j,t} = \sum_{k=1}^{4} w_{j,k} \cdot \tilde{s}_{k,t}, \quad w_{j,k} \in [-1,1]$$

Zur Normierung wird verwendet:

$$I_{j,t} = \frac{S_{j,t} - S_j^{min}}{S_j^{max} - S_j^{min}}$$

Dabei werden die Schranken approximiert durch:

$$S_j^{max} = \sum_{k:\, w_{j,k} > 0} w_{j,k}, \quad S_j^{min} = \sum_{k:\, w_{j,k} < 0} w_{j,k}$$

Diese Approximation erfolgt zur Laufzeit und gewährleistet eine robuste Skalierung auf das Intervall $[0,1]$.

---

### **3.3.2 Unternehmensvariablen**

- **Direkter Umsatz:**

$$u_t = b_t \cdot \frac{I_{u,t}^{1/3}}{0{,}5^{1/3}}$$

- **Zukünftige Investitionen:**

$$i_t = \frac{8}{3}\, I_{i,t}^2 + 3$$

- **Sozialpolitische Sichtbarkeit:**

$$s_t = I_{s,t}$$

Persistenz:

$$s_{t+1} = \begin{cases} I_{s,t+1}, & \text{falls Ereignis eintritt} \\ 0{,}5\, s_t + I_{s,t+1}, & \text{sonst} \end{cases}$$

- **Ethisches Verhalten:**

$$e_t = 3\, I_{e,t} - 1{,}5$$

---

## **3.4 Private Nutzenfunktionen der Agenten**

Jeder Agent besitzt drei private Nutzenkomponenten.

### **3.4.1 Berechnung**

Die Wirkung der Stellungsgrößen ergibt sich zu:

$$S_{p,l,t} = \sum_{k=1}^{4} w_{p,l,k} \cdot s_{k,t}, \quad w_{p,l,k} \in \{-1,0,1\}$$

Beschränkung:

$$S_{p,l,t} = \min\!\left(1,\, \max(0,\, S_{p,l,t}) \right)$$

Der Gesamtnutzen pro Runde ist:

$$p_t = \sum_{l=1}^{3} \left\lfloor 10 \cdot S_{p,l,t} \right\rfloor$$

---

### **3.4.2 Konfliktstruktur**

Die Agenten stehen in einem strukturellen Zielkonflikt zwischen individueller Nutzenmaximierung und der Wahrscheinlichkeit, dass ihr Vorschlag vom Principal akzeptiert wird. Aufgrund der privaten Natur der Nutzenfunktionen liegt ein Spiel unvollständiger Information vor.

---

## **3.5 Verhandlungsmechanismus**

Beide Agenten schlagen Budgetallokationen vor:

$$\mathbf{s}_t^{(A)}, \quad \mathbf{s}_t^{(B)}$$

Der Principal wählt:

$$\mathbf{s}_t^* \in \{\mathbf{s}_t^{(A)},\, \mathbf{s}_t^{(B)}\}$$

Der nicht gewählte Agent erhält einen reduzierten Nutzen:

$$p_t^{final} = \begin{cases} p_t, & \text{falls ausgewählt} \\ \left\lfloor 0{,}75 \cdot p_t \right\rfloor, & \text{sonst} \end{cases}$$

---

## **3.6 Designentscheidungen**

### **Zufällige Elemente**

- Personas
- Transformationsfunktionen
- Gewichtungen
- Rundenzahl

Diese Elemente reduzieren strategische Vorhersagbarkeit und erhöhen die Robustheit des Szenarios.

---

### **Komplexität**

Die Verwendung nichtlinearer Transformationen erzeugt bewusst eine hohe funktionale Komplexität, um reale Entscheidungsumgebungen mit schwer nachvollziehbaren Kausalitäten abzubilden.

---

## **3.7 Einordnung in die Principal-Agent-Theorie**

Das Modell integriert zentrale Problemstellungen der Principal-Agent-Theorie:

- Moral Hazard
- Hidden Information
- Hidden Action

Darüber hinaus erweitert es klassische Modelle durch:

- Mehragentensysteme mit Wettbewerb
- Dynamische Interaktionen
- Endogene Ressourcenentwicklung
- Stochastisches Spielende

---

## **3.8 Spieltheoretische Einordnung des implementierten Experiment-Designs**

Das tatsächlich durchgeführte Experiment weicht in mehreren Punkten vom theoretischen Idealmodell ab. Diese Abweichungen sind teilweise bewusste Designentscheidungen, die die externe Validität erhöhen, und teilweise praktische Kompromisse.

### **Abweichungen vom theoretischen Modell**

| Dimension | Theoretisches Modell | Implementiertes Design | Implikation |
|---|---|---|---|
| Rationalität | Vollständige Rationalität | BWL-Erstsemesterstudierende ohne VR-Vorerfahrung | Bounded Rationality zu erwarten (Simon 1955) |
| Spielende | Stochastisch, bekannte Verteilung | Stochastisch, Verteilung bekannt (min. 3 Runden) | Backward-Induction-Problem vermieden; Folk-Theorem-Bedingungen erfüllt |
| Kommunikation | Nur Allokationsvorschläge | Verbale Kommunikation + VR-Avatare | Cheap-Talk-Kanal zusätzlich vorhanden; nicht modelliert |
| Transformationsfunktionen | Bekannt im Modell | Unbekannt für Akteure | Erhöht kognitive Last erheblich; begünstigt Heuristiken |
| Nutzenfunktionen | Privat und stabil | Privat, durch Persona vorgegeben | Typen-Heterogenität wie in Adverse-Selection-Modellen |
| VR-Umgebung | Nicht modelliert | Vollimmersive VR-Umgebung (Meta Quest) | Präsenzerleben und Avatar-Effekte nicht im formalen Modell |
| Zeitdruck | Nicht modelliert | 3–5 Minuten pro Runde | Kognitiver Stress; verändert Entscheidungsqualität |

### **Gleichgewichtsanalyse des implementierten Designs**

Das implementierte Design ist ein unvollständiges Informationsspiel mit mehreren Agenten. Die spieltheoretisch relevanten Charakteristika sind:

**Typ 1: Bayesianisches Nash-Gleichgewicht unter unvollständiger Information (Harsanyi 1967)**
Da die Persona-Typen privat sind, liegt ein Spiel mit unvollständiger Information vor. Das bayesianische Gleichgewicht setzt voraus, dass der Principal Prior-Beliefs über Agenten-Typen aktualisiert. In endlichen Experimenten mit kurzer Zeitreihe ist diese Aktualisierung begrenzt möglich.

**Typ 2: Folk-Theorem-kompatibles Setting (Fudenberg & Maskin 1986)**
Das stochastische Spielende mit Fortsetzungswahrscheinlichkeit $P(t) = \frac{1}{t-2}$ für $t \geq 3$ erzeugt effektiv eine unendliche Horizont-Situation in den frühen Runden. Das Folk Theorem besagt, dass unter diesen Bedingungen ein breites Spektrum an kooperativen und nicht-kooperativen Gleichgewichten möglich ist. Konkret: Reputationsaufbau durch den Principal (oder durch Agenten) ist als Gleichgewichtsstrategie rationalisierbar.

**Typ 3: Relative Performance Evaluation (Holmström 1982)**
Da beide Agenten ihre Allokation dem Principal präsentieren und der Principal eine wählt, entsteht automatisch ein Vergleichsmechanismus — der Principal nutzt Agenten B als relativen Maßstab für Agenten A und umgekehrt. Dies eliminiert gemeinsame Schocks und erhöht Anreizintensität.

---

## **3.9 Hypothesenkatalog**

Der folgende Hypothesenkatalog leitet aus der spieltheoretischen Literatur sowie verwandten Disziplinen testbare Vorhersagen für die spezifischen Bedingungen des implementierten Experiments ab. Jede Hypothese ist einer Versuchsbedingung zugeordnet und mit einer Primärquelle belegt.

### **Cluster I: Wiederholtes Spiel und Reputationsaufbau**

**H1 — Folk-Theorem-Kooperation** *(Fudenberg & Maskin, 1986)*
> In einem wiederholten Spiel mit stochastischem Ende und hinreichend hoher Fortsetzungswahrscheinlichkeit sollten kooperative Strategien auf dem Gleichgewichtspfad erscheinen. Konkreter: Der Anteil von Allokationsvorschlägen, die die Unternehmensperformance maximieren (statt private Nutzen), sollte mit zunehmender Rundenzahl steigen.

**H2 — Reputation durch sequentielle Signale** *(Kreps & Wilson, 1982)*
> Sowohl Principal als auch Agenten können durch frühes strategisches Verhalten Reputation aufbauen. Vorhersage: Agenten, die in Runde 1 einen unternehmensdienlichen Vorschlag machen (auch auf Kosten ihrer Persona), werden in späteren Runden bevorzugt ausgewählt und sichern sich damit höhere Gesamtpunkte.

**H3 — Kein vollständiges Backward Induction** *(Selten, 1978 — Chain Store Paradox)*
> Bei endlichen Spielen mit vollständiger Rationalität würde Backward Induction Kooperation ausschließen. Das stochastische Spielende verhindert diesen Mechanismus: Teilnehmer können die letzte Runde nicht sicher identifizieren und spielen deshalb nicht-defizierende Strategien noch in späten Runden.

---

### **Cluster II: Drei Spieler und Moral Hazard**

**H4 — Relative Performance Evaluation** *(Holmström, 1982 — Moral Hazard in Teams)*
> Mit zwei konkurrierenden Agenten verwendet der Principal implizit eine relative Performance Evaluation: Er wählt den Agenten, dessen Vorschlag besser zur eigenen (unbekannten) Zielfunktion passt. Vorhersage: Agenten werden nicht nur die Unternehmensperformance optimieren, sondern auch versuchen, den Vorschlag des Gegners zu antizipieren und zu übertreffen (strategischer Wettbewerb).

**H5 — Adverse Selection durch Personas** *(Demski & Sappington, 1984)*
> Die zufällig zugewiesenen Personas erzeugen heterogene Typen (unterschiedliche private Nutzenfunktionen). Der Principal kann Typen ex ante nicht beobachten. Vorhersage: Agenten mit stark divergierenden Personas vom Unternehmensinteresse werden systematisch abgewählt; dieser Selektionseffekt verändert die Allokationsmuster über Runden.

**H6 — Koalitionsbildung gegen den Principal** *(Gamson, 1961)*
> In Dreiparteienverhandlungen ist Koalitionsbildung eine häufige Strategie, wenn zwei Parteien gemeinsame Interessen gegen eine dritte haben. Vorhersage: Wenn der Principal aus Sicht beider Agenten systematisch unfair alloziert, sollten Agenten implizite Koalitionsstrategien entwickeln (z. B. ähnliche Allokationsvorschläge, gegenseitige Unterstützung in verbaler Kommunikation).

---

### **Cluster III: Zeitdruck und kognitive Belastung**

**H7 — Zeitdruck und Entscheidungsqualität** *(Carnevale & Lawler, 1986; Stuhlmacher et al., 1998)*
> Zeitdruck führt zu vereinfachten Heuristiken. Mit 3–5 Minuten pro Runde und vier Inputvariablen mit unbekannten nichtlinearen Transformationen ist die kognitive Last hoch. Vorhersage: Agenten fokussieren systematisch auf 1–2 Variablen statt alle vier zu optimieren; Allokationsstrategien werden über Runden stereotyper (Anchoring-Effekt auf Vorrundenallokation).

**H8 — Zeitdruck und distributive Verhandlung** *(Pruitt & Kim, 1994)*
> Unter Zeitdruck tendieren Verhandlungsführer zu distributiven Strategien (Kuchenteilung statt Kuchenwachstum). Vorhersage: Je näher an der Rundengrenze ein Vorschlag eingereicht wird, desto stärker orientiert er sich am privaten Nutzen des Agenten, weniger an der Unternehmensperformance.

**H9 — Kognitiver Overload durch nichtlineare Transformationen** *(Sweller, 1988 — Cognitive Load Theory)*
> Nichtlineare und unbekannte Transformationsfunktionen erhöhen den intrinsischen kognitiven Load stark. Vorhersage: Teilnehmer werden die Inputs als Black Box behandeln und Allokationsstrategien durch Trial-and-Error oder soziales Lernen (Beobachtung der Outputs anderer) entwickeln, statt analytisch zu optimieren.

---

### **Cluster IV: Informationsasymmetrie und Cheap Talk**

**H10 — Cheap-Talk-Signaling** *(Crawford & Sobel, 1982)*
> Wenn Agenten private Information haben (Persona/Nutzenfunktion) und über einen verbalen Kommunikationskanal verfügen, entsteht Cheap Talk. Vorhersage: Agenten werden verbale Hinweise auf ihre Präferenzen geben, die strategisch verzerrt sind; der Principal lernt, diese Signale zu diskontieren. Über Runden sollte die Signaldichte abnehmen, wenn der Principal als misstrauisch wahrgenommen wird.

**H11 — Hidden-Information-Problem und Signalgleichgewicht** *(Akerlof, 1970; Spence, 1973)*
> Agenten mit hohem privatem Nutzen relativ zum Unternehmensinteresse (hohe Agenda-Divergenz) werden diesen Typ zu verschleiern suchen. Vorhersage: Agenten mit stark von der Unternehmensperformance abweichenden Personas zeigen weniger transparente Allokationsbegründungen und mehr strategische Ambiguität in der verbalen Kommunikation.

---

### **Cluster V: Soziale Präferenzen und Vertrauen**

**H12 — Reziprozität und Vertrauensaufbau** *(Berg, Dickhaut & McCabe, 1995)*
> Wenn der Principal in einer frühen Runde einen Vorschlag eines Agenten wählt und dieser Vorschlag die Unternehmensperformance verbessert, baut sich gegenseitiges Vertrauen auf. Vorhersage: Wiederholte Auswahl desselben Agenten sollte über Runden hinweg kooperativeres Verhalten dieses Agenten erzeugen (Reziprozitätsspirale).

**H13 — Inequity Aversion** *(Fehr & Schmidt, 1999)*
> Agenten, die wiederholt abgewählt werden, empfinden Ungerechtigkeit. Vorhersage: Wiederholt abgewählte Agenten zeigen in späteren Runden aggressivere Allokationsvorschläge oder Verweigerungsverhalten (Sabotage durch extreme Allokationen), die das Gesamtergebnis verschlechtern.

**H14 — Bounded Rationality und Satisficing** *(Simon, 1955)*
> Keine der Versuchspersonen ist in der Lage, die optimale Allokation zu berechnen. Vorhersage: Allokationsentscheidungen orientieren sich nicht am Optimum, sondern an einem satisfizierenden Schwellenwert; Entscheidungen verbessern sich mit Erfahrung (spätere Runden) nur geringfügig.

---

### **Cluster VI: VR-spezifische Effekte**

**H15 — Proteus-Effekt und Avatar-Verhalten** *(Yee & Bailenson, 2007)*
> Avatare beeinflussen das Verhalten ihrer Nutzer. Vorhersage: Teilnehmer, die im VR-Experiment einen dominanten Rang (Principal/CEO) einnehmen, verhalten sich selbstbewusster und treffen konfidentere Entscheidungen als in einer realen oder videobasierten Verhandlung; der Avatar-Typ moduliert Verhandlungsintensität.

**H16 — Erhöhte soziale Präsenz durch VR** *(Short, Williams & Christie, 1976)*
> VR-Umgebungen mit 3D-Avataren und räumlichem Audio erzeugen höhere soziale Präsenz als Text- oder Videokonferenz. Vorhersage: Die Wettbewerbsdynamik zwischen den Agenten sollte emotional intensiver erlebt werden als in einem entsprechenden Online-Experiment; qualitative Berichte sollten stärkeres Involvement zeigen.

**H17 — Media Richness und Kommunikationsqualität** *(Daft & Lengel, 1986)*
> VR bietet durch Avatar-Gestik, räumliche Nähe und synchrone Kommunikation eine höhere „Information Richness" als Textkanal oder 2D-Video. Vorhersage: Missverständnisse über Verhandlungsintentionen sollten in VR seltener auftreten als in textbasierten Vergleichsstudien; verbale und nonverbale Signale verstärken sich gegenseitig.

**H18 — Immersion und Entscheidungsqualität** *(Ding, Brinkman & Neerincx, 2020)*
> VR-Immersion steigert Engagement und Self-Efficacy in Verhandlungsszenarien. Vorhersage: Teilnehmer mit höherem Immersionserleben (gemessen per UEQ-S hedonischer Subskala) zeigen aktivere Verhandlungsstrategien und höhere Entscheidungsqualität als Teilnehmer mit niedrigerem Immersionserleben.

---

### **Hypothesen: Übersichtstabelle**

| Hypothese | Versuchsbedingung | Primärquelle | Framework-Domäne |
|---|---|---|---|
| H1 Folk-Theorem-Kooperation | Wiederholtes Spiel | Fudenberg & Maskin (1986) | WB / EU |
| H2 Reputationssignaling | Wiederholtes Spiel | Kreps & Wilson (1982) | WB / EU |
| H3 Kein Backward Induction | Stochastisches Ende | Selten (1978) | WB |
| H4 Relative Performance Eval. | Drei Spieler | Holmström (1982) | WB / EU |
| H5 Adverse Selection | Drei Spieler + Personas | Demski & Sappington (1984) | WB |
| H6 Koalitionsbildung | Drei Spieler | Gamson (1961) | WB / EU |
| H7 Zeitdruck + Heuristiken | Zeitdruck | Carnevale & Lawler (1986) | WB / EU |
| H8 Distributive Strategie | Zeitdruck | Pruitt & Kim (1994) | WB |
| H9 Kognitiver Overload | Nichtlineare Fkt. | Sweller (1988) | WB / EU |
| H10 Cheap-Talk-Signaling | Informationsasymmetrie | Crawford & Sobel (1982) | WB / EU |
| H11 Hidden Information | Informationsasymmetrie | Akerlof (1970) | WB |
| H12 Reziprozität | Vertrauen | Berg et al. (1995) | WB / EU |
| H13 Inequity Aversion | Vertrauen / Fairness | Fehr & Schmidt (1999) | WB / EU |
| H14 Bounded Rationality | Nichtlineare Fkt. | Simon (1955) | WB |
| H15 Proteus-Effekt | VR-Avatar | Yee & Bailenson (2007) | WB / VA |
| H16 Soziale Präsenz | VR-Umgebung | Short et al. (1976) | WB / VA |
| H17 Media Richness | VR-Umgebung | Daft & Lengel (1986) | WB / VA |
| H18 Immersion + Qualität | VR-Umgebung | Ding et al. (2020) | WB / EU |

---

## **3.10 Vergleich: Modellvorhersagen vs. beobachtetes Verhalten**

Dieser Abschnitt stellt die theoretischen Gleichgewichtsvorhersagen den empirischen Beobachtungen aus dem Workshop (n=15, 5 Gruppen, April 2026) gegenüber. Da kein Zugang zu den Rohdaten der Spielallokationen vorliegt, ist der Vergleich auf der qualitativen Ebene gehalten.

> **Ausstehend**: Quantitativer Vergleich der tatsächlichen Allokationsvektoren mit Gleichgewichtspfaden erfordert Exportdaten aus dem Unity-Spielclient. Dieser Schritt ist geplant, aber noch nicht durchgeführt.

### **Beobachtungen zur H1 (Folk-Theorem-Kooperation)**

**Vorhersage:** Kooperationsanteil steigt mit Rundenzahl.

**Beobachtung:** Qualitative Berichte zeigen, dass Flow-Phasen (gruppenspezifisches Engagement) erst ab Runde 2–3 einsetzten. In Gruppe 3 entstand ab Runde 2 eine ausgeprägte Wettbewerbsorientierung der Agenten gegenüber dem Principal — dies ist konsistent mit der Folk-Theorem-Vorhersage, wenngleich Wettbewerb statt Kooperation dominierte. Gruppe 5 zeigte CEO-zentriertes strategisches Handeln in späten Runden — kongruent mit Reputationsaufbau (H2).

**Fazit:** H1/H2 partiell bestätigt für Gruppen 3 und 5; kein eindeutiger Trend über alle Gruppen.

---

### **Beobachtungen zur H4 (Relative Performance Evaluation)**

**Vorhersage:** Agenten versuchen, den Konkurrenzvorschlag zu antizipieren.

**Beobachtung:** In den Kurzinterviews berichteten Teilnehmer von wettbewerbsorientiertem Verhalten. Die CIPD-Verhaltensbeobachtung zeigt strategische Zuwendungen (Kopfdrehen) zu dem jeweils anderen Agenten, was auf Monitoring des Konkurrenten hindeutet. In Gruppen 4 und 5 war strategisches Eigeninteresse klar erkennbar.

**Fazit:** H4 gestützt; expliziter Test erfordert Allokationsdaten.

---

### **Beobachtungen zu H7/H9 (Zeitdruck und Kognitiver Overload)**

**Vorhersage:** Agenten fokussieren auf 1–2 Variablen; Allokationen werden über Runden stereotyper.

**Beobachtung:** Die Fragen an die Versuchsleitung betrafen überwiegend die Simulationsmechanik (Inputs/Outputs), nicht die VR-Hardware. Die UEQ-S-Subskala „Übersichtlichkeit" zeigte mit SD=1,79 die höchste Streuung aller Items — ein direkter Indikator für kognitive Überforderung durch die Simulationsvariablen. Qualitative Berichte dokumentieren Confusion über Kausalzusammenhänge.

**Fazit:** H9 (kognitiver Overload durch nichtlineare Transformationen) klar bestätigt. H7 (Heuristiken unter Zeitdruck) plausibel, aber ohne Allokationsdaten nicht quantifizierbar.

---

### **Beobachtungen zu H10 (Cheap-Talk-Signaling)**

**Vorhersage:** Agenten geben strategisch verzerrte verbale Hinweise auf ihre Präferenzen.

**Beobachtung:** Teilnehmer berichteten überraschend offen über ihre Inputvariablen, während sie Private-Utility-Punkte geheimhielten. Dies entspricht einem Cheap-Talk-Gleichgewicht: Informationen über Inputs sind beobachtbar (kein Geheimnis), während der Transfer zur privaten Nutzenmaximierung verborgen bleibt. Das Principal-Konzept der „Hidden Agenda" hat die erwarteten selektiven Offenbarungsanreize erzeugt.

**Fazit:** H10 qualitativ bestätigt; das Design hat Cheap-Talk-Muster wie vorhergesagt induziert.

---

### **Beobachtungen zu H14 (Bounded Rationality)**

**Vorhersage:** Entscheidungen orientieren sich an zufriedenstellenden Schwellenwerten, nicht am Optimum.

**Beobachtung:** Keine Gruppe konnte die nichtlinearen Transformationsfunktionen analytisch lösen. Stattdessen entstanden gruppenspezifische Heuristiken (z. B. bevorzugte Allokation auf einzelne Stellgrößen, gleichmäßige Verteilung). Die VR-Umgebung hat diese heuristische Entscheidungsfindung nicht reduziert.

**Fazit:** H14 klar bestätigt; Simon's Bounded-Rationality-Konzept erklärt das Entscheidungsverhalten besser als das Optimierungsmodell.

---

### **Beobachtungen zu H16/H17/H18 (VR-spezifische Effekte)**

**Vorhersage:** VR erzeugt höhere soziale Präsenz und stärkere emotionale Beteiligung als alternative Formate.

**Beobachtung:** Immersion war mit 29 von 102 codierten Aussagen (28 %) die stärkste Kategorie der qualitativen Analyse. Teilnehmer beschrieben das Vergessen der realen Umgebung, motorische Impulse und erhöhtes Stresserleben in der Agentenrolle. Avatar-Gesten (deiktisch, soziale Zuwendung) wurden spontan ohne Training eingesetzt. Vergleich zu Zoom: VR wurde als „intensiver" und „präsenter" beschrieben.

**Fazit:** H16–H18 klar bestätigt. VR hat die emotionale Beteiligung und Wettbewerbsdynamik verstärkt, nicht abgeschwächt.

---

### **Zusammenfassung des Vergleichs**

| Hypothese | Evidenzlage | Bewertung |
|---|---|---|
| H1 Folk-Theorem-Kooperation | Partiell bestätigt (Gruppen 3, 5) | Qualitativ gestützt |
| H2 Reputationssignaling | Bestätigt (Gruppe 5) | Qualitativ gestützt |
| H3 Kein Backward Induction | Nicht widerlegt | Design-Schutz wirksam |
| H4 Relative Performance Eval. | Bestätigt | Qualitativ + CIPD |
| H5 Adverse Selection | Plausibel | Nicht direkt testbar (keine Rohdaten) |
| H6 Koalitionsbildung | Nicht eindeutig beobachtet | Offen |
| H7 Zeitdruck + Heuristiken | Plausibel | Qualitativ indiziert |
| H9 Kognitiver Overload | Klar bestätigt | UEQ-S + Qualitativ |
| H10 Cheap-Talk-Signaling | Bestätigt | Qualitativ + Beobachtung |
| H14 Bounded Rationality | Klar bestätigt | Qualitativ + Beobachtung |
| H16–H18 VR-Präsenz + Immersion | Klar bestätigt | UEQ-S + Qualitativ |

**Offene Fragen (erfordern Allokationsrohdaten):**
- Quantitative Überprüfung von H1–H5 über Allokationsvektoren
- Identifikation von Reputationsstrategien aus sequentiellen Allokationsdaten
- Messung der Allokationskonvergenz über Runden (Stereotypisierungseffekt aus H7)

---
