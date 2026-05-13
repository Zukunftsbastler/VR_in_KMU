# Entwurf: Virtuelles Messeszenario in VR (Fallstudie VR-Messestand)

> **Zielstelle im Buch:** `Buch/06_empirische_untersuchung.md`
> Einzufügen als neuer Abschnitt nach H2 (360°-Fotografie) als Praxisexperiment H3.
> Überschriftenebene: `##` (gleichwertig mit H1 und H2)
>
> **Framework-Verortung:** VA (VR-Eignung für Produktpräsentation und Messe-Szenarien), TI (3D-Content-Integration)
> **Testfall-Relevanz:** noch zuzuordnen
>
> **⚠️ Offene Punkte — vor Fertigstellung zu klären:**
> - Einverständnis der beteiligten Partner (Orion / Omnicon Group / Neox Studios) zur namentlichen Nennung
> - Welche Partner / Unternehmen haben teilgenommen, und mit welchen Produkten?
> - Welche 3D-Modelle lagen vor, und in welchem Format (FBX, OBJ, CAD-Export …)?
> - Eingesetzte VR-Hardware (z. B. Meta Quest 2/3, PC-VR)
> - Qualitative oder quantitative Ergebnisse (Akzeptanz, wahrgenommener Nutzen, Grenzen) zum Messe-Hauptszenario
> - Vergleich mit physischer Messe: Erreichbarkeit, Kosten, Interaktionstiefe
> - Wie wurden Stände ohne vorliegende 3D-Modelle behandelt?
> - Mehrbenutzer-Betrieb: Konnten mehrere Personen gleichzeitig die virtuelle Messe besuchen?
> - **Gestenperzeptionstest (aus Videoanalyse):** Fehlerquote aufgeschlüsselt nach Distanzbedingung (nah ~2,5 m vs. fern ~6,5 m)? Gab es in Runde 2 Unterschiede bei variierter Distanz? Subjektive Einschätzungen der Teilnehmenden? → Protokolldaten beim Moderator / Versuchsleiter erfragen

---

## Praxisexperiment H3: Virtuelles Messeszenario als VR-Applikation

### Zielsetzung und Versuchsaufbau

<!-- TODO: Zielsetzung beschreiben — welche Frage sollte das Experiment beantworten?
     Warum Messe-Szenario? Welche KMU-Relevanz? Welche Partner waren beteiligt und warum? -->

Im Rahmen des Projekts wurde erprobt, ob sich ein virtuelles Messeszenario als Alternative oder Ergänzung zu physischen Messen eignet. Anders als bei einer realen Messe findet das Szenario vollständig in einer VR-Umgebung statt: Beteiligte Partnerunternehmen präsentieren ihre Produkte an virtuellen Messeständen, sofern entsprechende 3D-Modelle vorliegen. Die Applikation wurde mit **Unity** entwickelt.

### Aufbau der VR-Umgebung

<!-- TODO: Aufbau der virtuellen Messehalle beschreiben — Layout, Anzahl Stände, Navigation,
     Atmosphäre / visuelles Design. Wie wurde der Raum gestaltet? -->

**Virtuelle Messestände:**
Jeder beteiligte Partner erhielt einen eigenen virtuellen Messestand, an dem seine Produkte in Form von **3D-Modellen** präsentiert werden konnten. Die Einbindung setzte voraus, dass geeignete 3D-Daten der Produkte vorlagen.

**Produktpräsentation:**

<!-- TODO: Wie wurden die 3D-Modelle im Stand dargestellt? Interaktionsmöglichkeiten?
     Konnten Objekte skaliert, gedreht oder inspiziert werden? -->

**Navigation:**

<!-- TODO: Wie bewegten sich Nutzer durch die virtuelle Messe?
     Teleportation, freie Bewegung, geführte Tour? -->

### Beobachtungen

<!-- TODO: Beobachtungen zum Messe-Hauptszenario eintragen — was funktionierte gut?
     Wo gab es Probleme (fehlende Modelle, technische Hürden, Orientierung in der VR-Umgebung)? -->

#### Begleitexperiment: Gestenperzeptionstest in der virtuellen Messehalle

*Quelle: Videoanalyse der Session-Aufzeichnungen. Die nachfolgende Beschreibung basiert auf der Beobachtung der Videos; die Zielsetzung des Versuchsleiters ist nicht dokumentiert und wurde aus dem Versuchsprotokoll rekonstruiert.*

Im Rahmen der Session wurde ein strukturiertes Begleitexperiment zur nonverbalen Kommunikation in VR durchgeführt. Fünf Personen (Versuchsleiter + vier Teilnehmende) standen in einem Kreis in der virtuellen Messehalle. Die Avatare bestanden aus **Kopf und zwei Händen** — keine Arm-, Torso- oder Beindarstellung, wie es für Meta-Quest-basierte Systeme typisch ist. Zur Identifikation war jeder Avatar in einer individuellen Farbe gehalten; die Teilnehmenden wurden im Protokoll ausschließlich durch ihre Farbe bezeichnet.

**Versuchsprotokoll (zwei Runden):**

*Runde 1 — Distanzvergleich:*
1. Der Moderator (in dieser Runde: der Versuchsleiter) nimmt eine Körperhaltung bzw. Geste ein (z. B. linke Hand weit über den Kopf gestreckt, rechte Hand hängend).
2. Eine Teilnehmerin / ein Teilnehmer wird aufgefordert, die Geste verbal zu beschreiben — zunächst aus **kurzer Distanz (~2,5 m)**.
3. Die beschreibende Person stellt ihre Beschreibung zur Bestätigung: „Ist das richtig?"
4. Der Moderator bestätigt oder korrigiert.
5. Dieselbe Person beschreibt die Geste unmittelbar anschließend ein zweites Mal aus **größerer Distanz (~6,5 m)** — wiederum mit Bestätigungsschleife.
6. Die Abfolge (Nahbeschreibung → Fernbeschreibung) wird mit allen vier Teilnehmenden jeweils einmal wiederholt.

*Runde 2 — Rollenwechsel mit Distanzvariation:*
7. Die Person, die zuletzt beschrieben hat, übernimmt die Rolle des **Moderators** und nimmt eine neue Geste ein.
8. Explizite Anforderung: Der nächste Beschreibende soll **nicht immer** der direkte Nachbar sein — die Distanz zwischen Moderator und Beschreibendem soll über die Runden hinweg variieren.
9. Beschreibung → Bestätigung → Rollenwechsel setzt sich fort, bis jede Person mindestens einmal Moderator und einmal Beschreibender war.

**Methodische Struktur:**  
Das Protokoll kombiniert zwei Variablen: **Rolle** (Moderator vs. Beschreibender, vollständig ausbalanciert) und **Distanz** (Nah ~2,5 m vs. Fern ~6,5 m in Runde 1; freie Variation in Runde 2). Die explizite Bestätigungsschleife („Ist das richtig?") schafft ein binäres Korrektheitssignal pro Beschreibungsversuch und ermöglicht einen direkten Vergleich der Gestenperzeptionsgenauigkeit zwischen den Distanzbedingungen.

### Ergebnisse

<!-- TODO: Ergebnisse zum Messe-Hauptszenario nach Vorliegen der Nutzerdaten ergänzen. -->

#### Vorläufige Befunde aus dem Gestenperzeptionstest

*Hinweis: Da keine Protokolldaten vorliegen, sind die folgenden Aussagen aus der Videobeobachtung abgeleitet und müssen durch den Versuchsleiter validiert werden.*

Die Videoanalyse legt nahe, dass Teilnehmende in der Lage waren, Avatargesten trotz fehlender Arm- und Torsodarstellung zu beschreiben und verbal zu kommunizieren. Die räumliche Beziehung zwischen Kopf und Händen scheint als Trägersignal für Gestenerkennung auszureichen — ein Befund, der mit der körpersprach-reduzierten Darstellung von Consumer-VR-Hardware konsistent ist.

<!-- TODO: Ergänzen — wie viele Gesten wurden korrekt erkannt, aufgeschlüsselt nach Distanz (nah vs. fern)?
     Gab es in einer der beiden Distanzbedingungen mehr Fehlbeschreibungen?
     Wie reagierten die Teilnehmenden auf Korrekturen des Moderators?
     Subjektive Einschätzungen zur wahrgenommenen Schwierigkeit bei naher vs. ferner Distanz? -->

### Einordnung und Handlungsempfehlung

<!-- TODO: Bewertung des Messe-Hauptszenarios — für welche KMU-Szenarien geeignet?
     Welche Voraussetzungen müssen erfüllt sein (3D-Modelle, Budget, technisches Know-how)?
     Vergleich mit physischer Messe und mit anderen VR-Präsentationsformen. -->

#### Einordnung des Gestenperzeptionstests: Nonverbale Kommunikation mit minimalen Avataren

Das Experiment adressiert eine für den KMU-Einsatz von VR-Messen praktisch relevante Frage: Auf physischen Messen ist Körpersprache ein zentrales Kommunikationsmittel — Aussteller zeigen auf Produkte, demonstrieren Dimensionen durch Gesten, signalisieren Einladung oder Ablehnung. Wenn VR-Plattformen diesen Kanal nicht oder nur eingeschränkt übertragen, verliert das Format einen wesentlichen Teil seines Interaktionswerts.

Die gezielte Variation der Beobachtungsdistanz (Nah ~2,5 m vs. Fern ~6,5 m) macht **Distanz zur unabhängigen Variable** des Experiments. Dies ist für Messe-Szenarien besonders relevant: Ein typischer Messestand hat eine Tiefe von mehreren Metern; Ausstellende und Besuchende interagieren auf wechselnden Abständen. Ob Gesten auch auf größere VR-Distanz hinreichend erkennbar bleiben, bestimmt, wie großzügig eine virtuelle Messehalle gestaltet werden kann, ohne Kommunikationsqualität einzubüßen.

Die vorläufigen Befunde aus der Videoanalyse legen folgende Einschätzungen nahe:

- **Für KMU-Entscheider:** Consumer-VR-Hardware (Meta Quest) liefert keine Körper- oder Armdarstellung — die räumliche Beziehung zwischen Kopf und Händen scheint als Trägersignal für Gestenerkennung gleichwohl auszureichen. Ein teures Upgrade auf Full-Body-Tracking ist für einfache Präsentationsszenarien vermutlich nicht erforderlich.
- **Für das Raumdesign virtueller Messen:** Sollte die Fehlerquote bei ~6,5 m spürbar ansteigen, ergibt sich eine praxisrelevante Empfehlung für maximale Interaktionsdistanzen in VR-Messeumgebungen. Sollte sie stabil bleiben, wäre das ein starkes Argument für großzügig dimensionierte virtuelle Hallen.
- **Für die Plattformentwicklung:** Die Farbkodierung der Avatare erwies sich als einfaches, aber wirksames Identifikationsmittel in Mehrpersonenszenarien — besonders wenn Moderator und Beschreibende nicht in direkter Nachbarschaft stehen.
- **Für zukünftige Studien:** Das Protokoll (Nah/Fern-Paar pro Person, Moderator-Rollenwechsel mit Distanzvariation) ist methodisch schlank und replizierbar. Es könnte als standardisierter Kommunikationsqualitätstest am Beginn von VR-Meeting-Experimenten eingesetzt werden.

<!-- TODO: Sobald Protokolldaten vorliegen — Fehlerquoten nach Distanzbedingung ergänzen
     und die vorläufige Einordnung entsprechend belegen oder korrigieren. -->

> **Methodische Transparenz:** Die Zielsetzung des Gestenperzeptionstests ist bislang nicht formal dokumentiert; die Einordnung basiert auf der Videoanalyse und der Rekonstruktion des Versuchsprotokolls. Belastbare quantitative Aussagen — insbesondere zum Distanzeffekt — erfordern die Protokolldaten des Moderators.
