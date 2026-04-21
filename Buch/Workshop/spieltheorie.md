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
