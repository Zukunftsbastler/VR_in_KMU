# **3\. Spieltheoretische Modellierung eines dynamischen Principal-Agent-Szenarios**

## **3.1 Einleitung**

Das in dieser Arbeit entwickelte Workshop-Szenario modelliert eine dynamische Mehrrundenverhandlung unter asymmetrischer Information auf Basis des Principal-Agent-Ansatzes. Im Zentrum steht die Interaktion zwischen drei Akteuren: einem Principal (CEO) sowie zwei Agenten (Manager A und Manager B).

Jeder Akteur erhält zu Beginn des Szenarios eine zufällig ausgewählten Persona, welche individuelle Präferenzen und Zielsetzungen definiert. Diese Präferenzen sind privat und für die jeweils anderen Akteure nicht beobachtbar, wodurch eine klassische Informationsasymmetrie entsteht.

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

Zu Beginn jeder Runde t∈Nt \\in \\mathbb{N}t∈N steht ein Budget bt\>0b\_t \> 0bt​\>0 zur Verfügung, wobei für die erste Runde gilt:

b1=15b\_1 \= 15b1​=15

Die Agenten verteilen das Budget auf vier Stellungsgrößen sk,t∈\[0,1\]s\_{k,t} \\in \[0,1\]sk,t​∈\[0,1\] mit k=1,…,4k \= 1, \\dots, 4k=1,…,4. Die Gesamtallokation ist beschränkt durch:

∑k=14sk,t≤43\\sum\_{k=1}^{4} s\_{k,t} \\leq \\frac{4}{3}k=1∑4​sk,t​≤34​

Das verbleibende Budget nach Allokation ergibt sich zu:

btres=bt(1−13∑k=14sk,t)b\_t^{res} \= b\_t \\left(1 \- \\frac{1}{3} \\sum\_{k=1}^{4} s\_{k,t} \\right)btres​=bt​(1−31​k=1∑4​sk,t​)

Diese Formulierung erlaubt eine Überallokation des Budgets bis zu 133 %, was zur Aufnahme von Schulden führt.

---

### **Verschuldung**

Im Falle einer Überallokation (btres\<0b\_t^{res} \< 0btres​\<0) wird ein Kredit mit einem Zinssatz von 100 % aufgenommen. Das effektive Budget ergibt sich somit zu:

btfinal={btres,falls btres≥02⋅btres,falls btres\<0b\_t^{final} \= \\begin{cases} b\_t^{res}, & \\text{falls } b\_t^{res} \\geq 0 \\\\ 2 \\cdot b\_t^{res}, & \\text{falls } b\_t^{res} \< 0 \\end{cases}btfinal​={btres​,2⋅btres​,​falls btres​≥0falls btres​\<0​

---

### **3.2.3 Spielende**

Das Spiel endet entweder durch Insolvenz (btfinal\<0b\_t^{final} \< 0btfinal​\<0) oder durch ein stochastisches Abbruchkriterium ab Runde t≥3t \\geq 3t≥3.

Die Fortsetzungswahrscheinlichkeit ist definiert als:

P(Fortsetzung in Runde t)={1,t\<31t−2,t≥3P(\\text{Fortsetzung in Runde } t) \= \\begin{cases} 1, & t \< 3 \\\\ \\frac{1}{t \- 2}, & t \\geq 3 \\end{cases}P(Fortsetzung in Runde t)={1,t−21​,​t\<3t≥3​

Diese Konstruktion impliziert eine mit zunehmender Rundenzahl sinkende Fortsetzungswahrscheinlichkeit.

---

## **3.3 Unternehmensdynamik**

Die Entwicklung des Unternehmens wird durch vier zentrale Outputgrößen bestimmt:

* Direkter Umsatz utu\_tut​  
* Zukünftige Investitionen iti\_tit​  
* Sozialpolitische Sichtbarkeit sts\_tst​  
* Ethisches Verhalten ete\_tet​

Das Budget der folgenden Runde ergibt sich zu:

bt+1=btfinal+it−1⋅ut+1{xt\<st}⋅et⋅10⋅t2b\_{t+1} \= b\_t^{final} \+ i\_{t-1} \\cdot u\_t \+ \\mathbb{1}\_{\\{x\_t \< s\_t\\}} \\cdot e\_t \\cdot 10 \\cdot t^2bt+1​=btfinal​+it−1​⋅ut​+1{xt​\<st​}​⋅et​⋅10⋅t2

mit einer Zufallsvariable:

xt∼U(0,1)x\_t \\sim \\mathcal{U}(0,1)xt​∼U(0,1)

Für die Initialisierung gilt:

i0=1i\_0 \= 1i0​=1

Die sozialpolitische Sichtbarkeit sts\_tst​ bestimmt die Eintrittswahrscheinlichkeit eines externen Ereignisses, dessen Wirkung durch das ethische Verhalten ete\_tet​ moduliert wird.

---

### **3.3.1 Funktionale Zusammenhänge**

Die Outputgrößen basieren auf transformierten Stellungsgrößen:

s\~k,t=ek(sk,t)\\tilde{s}\_{k,t} \= e\_k(s\_{k,t})s\~k,t​=ek​(sk,t​)

Die Transformationsfunktionen werden in jeder Runde zufällig zugewiesen und sind den Akteuren nicht bekannt.

**Transformationsfunktionen:**

* Linear:

f(x)=ax,a∈(0,1)f(x) \= a x, \\quad a \\in (0,1)f(x)=ax,a∈(0,1)

* Stufenfunktion:

g(x)={0,x\<0,330,5,0,33≤x\<0,661,x≥0,66g(x) \= \\begin{cases} 0, & x \< 0{,}33 \\\\ 0{,}5, & 0{,}33 \\leq x \< 0{,}66 \\\\ 1, & x \\geq 0{,}66 \\end{cases}g(x)=⎩⎨⎧​0,0,5,1,​x\<0,330,33≤x\<0,66x≥0,66​

* Ease-In-Out:

h(x)={2x2,x\<0,51−(−2x+2)22,x≥0,5h(x) \= \\begin{cases} 2x^2, & x \< 0{,}5 \\\\ 1 \- \\frac{(-2x \+ 2)^2}{2}, & x \\geq 0{,}5 \\end{cases}h(x)={2x2,1−2(−2x+2)2​,​x\<0,5x≥0,5​

* Sinusfunktion:

i(x)=0,5+14\[sin⁡(3π2+2πx)+sin⁡(3π2+5πx)\]i(x) \= 0{,}5 \+ \\frac{1}{4} \\left\[ \\sin\\left(\\frac{3\\pi}{2} \+ 2\\pi x\\right) \+ \\sin\\left(\\frac{3\\pi}{2} \+ 5\\pi x\\right) \\right\]i(x)=0,5+41​\[sin(23π​+2πx)+sin(23π​+5πx)\]

---

Die aggregierte Wirkung auf eine Unternehmensvariable j∈{u,i,s,e}j \\in \\{u,i,s,e\\}j∈{u,i,s,e} ergibt sich zu:

Sj,t=∑k=14wj,k⋅s\~k,t,wj,k∈\[−1,1\]S\_{j,t} \= \\sum\_{k=1}^{4} w\_{j,k} \\cdot \\tilde{s}\_{k,t}, \\quad w\_{j,k} \\in \[-1,1\]Sj,t​=k=1∑4​wj,k​⋅s\~k,t​,wj,k​∈\[−1,1\]

Zur Normierung wird verwendet:

Ij,t=Sj,t−SjminSjmax−SjminI\_{j,t} \= \\frac{S\_{j,t} \- S\_j^{min}}{S\_j^{max} \- S\_j^{min}}Ij,t​=Sjmax​−Sjmin​Sj,t​−Sjmin​​

Dabei werden die Schranken approximiert durch:

Sjmax=∑k:wj,k\>0wj,k,Sjmin=∑k:wj,k\<0wj,kS\_j^{max} \= \\sum\_{k: w\_{j,k} \> 0} w\_{j,k}, \\quad S\_j^{min} \= \\sum\_{k: w\_{j,k} \< 0} w\_{j,k}Sjmax​=k:wj,k​\>0∑​wj,k​,Sjmin​=k:wj,k​\<0∑​wj,k​

Diese Approximation erfolgt zur Laufzeit und gewährleistet eine robuste Skalierung auf das Intervall \[0,1\]\[0,1\]\[0,1\].

---

### **3.3.2 Unternehmensvariablen**

* **Direkter Umsatz:**

ut=bt⋅Iu,t1/30,51/3u\_t \= b\_t \\cdot \\frac{I\_{u,t}^{1/3}}{0{,}5^{1/3}}ut​=bt​⋅0,51/3Iu,t1/3​​

* **Zukünftige Investitionen:**

it=83Ii,t2+3i\_t \= \\frac{8}{3} I\_{i,t}^2 \+ 3it​=38​Ii,t2​+3

* **Sozialpolitische Sichtbarkeit:**

st=Is,ts\_t \= I\_{s,t}st​=Is,t​

Persistenz:

st+1={Is,t+1,falls Ereignis eintritt0,5st+Is,t+1,sonsts\_{t+1} \= \\begin{cases} I\_{s,t+1}, & \\text{falls Ereignis eintritt} \\\\ 0{,}5 s\_t \+ I\_{s,t+1}, & \\text{sonst} \\end{cases}st+1​={Is,t+1​,0,5st​+Is,t+1​,​falls Ereignis eintrittsonst​

* **Ethisches Verhalten:**

et=3Ie,t−1,5e\_t \= 3 I\_{e,t} \- 1{,}5et​=3Ie,t​−1,5

---

## **3.4 Private Nutzenfunktionen der Agenten**

Jeder Agent besitzt drei private Nutzenkomponenten.

### **3.4.1 Berechnung**

Die Wirkung der Stellungsgrößen ergibt sich zu:

Sp,l,t=∑k=14wp,l,k⋅sk,t,wp,l,k∈{−1,0,1}S\_{p,l,t} \= \\sum\_{k=1}^{4} w\_{p,l,k} \\cdot s\_{k,t}, \\quad w\_{p,l,k} \\in \\{-1,0,1\\}Sp,l,t​=k=1∑4​wp,l,k​⋅sk,t​,wp,l,k​∈{−1,0,1}

Beschränkung:

Sp,l,t=min⁡(1,max⁡(0,Sp,l,t))S\_{p,l,t} \= \\min\\left(1, \\max(0, S\_{p,l,t}) \\right)Sp,l,t​=min(1,max(0,Sp,l,t​))

Der Gesamtnutzen pro Runde ist:

pt=∑l=13⌊10⋅Sp,l,t⌋p\_t \= \\sum\_{l=1}^{3} \\left\\lfloor 10 \\cdot S\_{p,l,t} \\right\\rfloorpt​=l=1∑3​⌊10⋅Sp,l,t​⌋

---

### **3.4.2 Konfliktstruktur**

Die Agenten stehen in einem strukturellen Zielkonflikt zwischen individueller Nutzenmaximierung und der Wahrscheinlichkeit, dass ihr Vorschlag vom Principal akzeptiert wird. Aufgrund der privaten Natur der Nutzenfunktionen liegt ein Spiel unvollständiger Information vor.

---

## **3.5 Verhandlungsmechanismus**

Beide Agenten schlagen Budgetallokationen vor:

st(A),st(B)\\mathbf{s}\_t^{(A)}, \\quad \\mathbf{s}\_t^{(B)}st(A)​,st(B)​

Der Principal wählt:

st∗∈{st(A),st(B)}\\mathbf{s}\_t^\* \\in \\{\\mathbf{s}\_t^{(A)}, \\mathbf{s}\_t^{(B)}\\}st∗​∈{st(A)​,st(B)​}

Der nicht gewählte Agent erhält einen reduzierten Nutzen:

ptfinal={pt,falls ausgewa¨hlt⌊0,75⋅pt⌋,sonstp\_t^{final} \= \\begin{cases} p\_t, & \\text{falls ausgewählt} \\\\ \\left\\lfloor 0{,}75 \\cdot p\_t \\right\\rfloor, & \\text{sonst} \\end{cases}ptfinal​={pt​,⌊0,75⋅pt​⌋,​falls ausgewa¨hltsonst​

---

## **3.6 Designentscheidungen**

### **Zufällige Elemente**

* Personas  
* Transformationsfunktionen  
* Gewichtungen  
* Rundenzahl

Diese Elemente reduzieren strategische Vorhersagbarkeit und erhöhen die Robustheit des Szenarios.

---

### **Komplexität**

Die Verwendung nichtlinearer Transformationen erzeugt bewusst eine hohe funktionale Komplexität, um reale Entscheidungsumgebungen mit schwer nachvollziehbaren Kausalitäten abzubilden.

---

## **3.7 Einordnung in die Principal-Agent-Theorie**

Das Modell integriert zentrale Problemstellungen der Principal-Agent-Theorie:

* Moral Hazard  
* Hidden Information  
* Hidden Action

Darüber hinaus erweitert es klassische Modelle durch:

* Mehragentensysteme mit Wettbewerb  
* Dynamische Interaktionen  
* Endogene Ressourcenentwicklung  
* Stochastisches Spielende

---

 