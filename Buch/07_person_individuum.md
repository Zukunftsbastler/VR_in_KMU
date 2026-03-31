---
title: "Person und Individuum"
---

## Individuelle Einflussfaktoren auf VR-Akzeptanz

Die Akzeptanz und Nutzungsintention von VR-Technologie variiert erheblich zwischen Individuen. Das UTAUT-Modell (QUELLE: venkatesh2003) identifiziert Alter, Geschlecht und Erfahrung als zentrale Moderatoren. Für den Unternehmenskontext sind folgende individuelle Faktoren besonders relevant:

## Technikaffinität (ATI)

Die Affinity for Technology Interaction (ATI) nach Franke et al. (2019) misst die intrinsische Motivation, sich mit technischen Systemen auseinanderzusetzen. Personen mit hoher ATI:

- Lernen neue Technologien schneller
- Erleben weniger Frustration bei technischen Problemen
- Sind bereit, länger mit unbekannten Systemen zu experimentieren

Für VR-Implementierungen in KMU empfiehlt sich, ATI bei der Auswahl von Pilotnutzern zu berücksichtigen.

## VR-Erfahrung und Lernkurve

Erstnutzer benötigen eine Eingewöhnungsphase von typischerweise 10–20 Minuten. Mit zunehmender Erfahrung sinkt die kognitive Last der Bedienung, und Nutzer können sich stärker auf die inhaltliche Aufgabe konzentrieren. Unternehmen sollten ausreichend Zeit für VR-Onboarding einplanen.

## Simulator Sickness / Motion Sickness

VR-Sickness (auch Cybersickness) ist ein bedeutendes Adoptionshemmnis. Symptome umfassen Übelkeit, Schwindel und Orientierungslosigkeit. Auslöser sind:

- Hohe Latenz zwischen Kopfbewegung und Bildaktualisierung (>20ms kritisch)
- Niedrige Bildwiederholrate (<90Hz problematisch)
- Aggressive Locomotion (künstliche Fortbewegung in VR)

Etwa 5–10% der Bevölkerung reagieren stark sensibel. Proaktive Screenings mit dem FMS-Fragebogen sind empfehlenswert (QUELLE: sitzmann2011).

## Alter und Generationsunterschiede

Ältere Nutzer zeigen im Durchschnitt höheren Effort Expectancy (größerer wahrgenommener Aufwand), profitieren aber gleichzeitig von spezifischen VR-Anwendungen wie immersiven Trainings. Angepasste Schulungsformate für verschiedene Altersgruppen sind wichtig (QUELLE: venkatesh2003).

## Psychologische Sicherheit

Die Bereitschaft, Fehler in VR zu machen und zu lernen, hängt stark von der psychologischen Sicherheit im Team ab. VR bietet hier einen Vorteil: Das Scheitern in der virtuellen Umgebung hat keine realen Konsequenzen, was Lernbereitschaft und Risikofreude fördert.

## Empfehlungen für KMU

- Erheben Sie ATI und VR-Vorerfahrung vor Pilotprojekten
- Starten Sie mit technikaffinen Early Adopters als Multiplikatoren
- Planen Sie ausreichend Onboarding-Zeit ein
- Bieten Sie Opt-out-Möglichkeiten bei Unwohlsein ohne Stigma
- Entwickeln Sie altersgerechte Schulungsformate

---

## Framework-Position und Querverweise

Diese Domäne deckt im Framework folgende Sub-Knoten ab: *Person*, *Körperliche Ausprägungen*, *Mentale Einschränkung*, *Technische Einschränkung*, *Alter*, *Offenheit*, *VR Adaptionsfähigkeit*.

### Verbindungen zu anderen Domänen

**→ Kap. 04: VR-Anwendungsszenarien**
*VR Adaptionsfähigkeit* ist ein geteilter Framework-Knoten. In Kap. 04 bezeichnet er die Eignung eines *Szenarios* für VR (Merkmal des Meetings). In Kap. 07 bezeichnet er die Fähigkeit einer *Person*, VR zu nutzen (Merkmal des Individuums). Die praktische Verbindung: Das VR-Kompatibilitätsurteil über ein Szenario (Kap. 04) muss mit dem Personenprofil der Teilnehmer (Kap. 07) abgeglichen werden. Ein hochgeeignetes Szenario wird scheitern, wenn ein relevanter Anteil der Belegschaft geringe ATI-Werte oder hohe Motion-Sickness-Anfälligkeit aufweist — und umgekehrt kann ein eher mittelmäßig geeignetes Szenario mit gut vorbereiteten, technikaffinen Teilnehmern erfolgreich sein.

**→ Kap. 03: Betriebswirtschaftlicher Nutzen**
*Individuelle VR Adaptionsfähigkeit* ist bei BN ein Sub-Knoten unter *Personalressourcen*. In Kap. 07 wird dieser Faktor detailliert. Was in Kap. 03 als Kostenfaktor erscheint (Kompetenzentwicklungsmaßnahmen, Schulungsaufwand), lässt sich nur dann realistisch kalkulieren, wenn bekannt ist, wie weit die Belegschaft von VR-Kompetenz entfernt ist. *Offenheit* und *Alter* (Kap. 07) modulieren den Schulungsbedarf und damit die Investitionsplanung in Kap. 03.

**→ Kap. 06: Empirische Untersuchung**
*Studienteilnehmer* (EU) werden nach P-Kriterien ausgewählt und charakterisiert: ATI-Wert und VR-Vorerfahrung als Auswahlkriterien; Altersverteilung und Geschlecht als Kontrollvariablen. Die heterogene Gruppenkomposition nach ATI im eigenen Workshop (Kap. 06) basiert direkt auf dem in Kap. 07 beschriebenen Befund, dass ATI ein signifikanter Moderator der Eingewöhnungsgeschwindigkeit ist. Nur wenn P-Variablen im Studiendesign kontrolliert werden, sind Verhaltensdaten aus EU interpretierbar.

---

## Praxisbeispiele

---

**Adaptive Avatar-Repräsentation in VR — Piumsomboon et al. (2018)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Forschungsprojekt |
| **Organisation** | University of Canterbury, Neuseeland |
| **Branche** | HCI / Mixed Reality |
| **Region** | Neuseeland / Australien |
| **Link / Quelle** | Piumsomboon et al. (2018), *CHI 2018*, ACM (QUELLE: piumsomboon2018mini) |
| **Rolle von VR** | VR-Avatar-System, das sich adaptiv an die Körpergröße und Blickrichtung des Gegenübers anpasst — „Mini-Me": der eigene Avatar erscheint für den anderen Teilnehmer skaliert und ausgerichtet |
| **Relevanz für P** | VR Adaptionsfähigkeit, Körperliche Ausprägungen (Körpergröße, Bewegungsradius), Technische Einschränkung |

**Beschreibung**: Das Mini-Me-System ermöglicht Mixed-Reality-Collaboration zwischen einem VR-Nutzer und einem AR-Nutzer (HoloLens): Der VR-Nutzer erscheint dem AR-Nutzer als skalierbarer kleiner Avatar auf dem realen Arbeitsplatz, während der AR-Nutzer dem VR-Nutzer als lebensgroße holographische Projektion erscheint. Das System reagiert auf die individuelle Körpergröße, Griffweite und Armlänge der Nutzer. Piumsomboon et al. zeigen, dass adaptive Avatare die wahrgenommene Präsenz und Aufgabenkoordination signifikant verbessern — insbesondere wenn physische Größenunterschiede zwischen Teilnehmern bestehen.

**Erkenntnisse für KMU**: Körperliche Ausprägungen sind in VR-Meetings nicht neutral. Mitarbeiter mit körperlichen Einschränkungen (Sehbehinderung, Bewegungseinschränkung, Größenextreme) werden durch schlecht kalibrierte Avatarsysteme benachteiligt. Für KMU bedeutet das: VR-Plattformwahl sollte die Anpassbarkeit von Avataren und Interaktionsradius explizit berücksichtigen. Das Mini-Me-System zeigt zudem das Potenzial hybrider VR/AR-Settings — relevant für KMU, die nicht alle Mitarbeiter mit Headsets ausstatten können (→ Kap. 04: Microsoft Mesh).

---

**Cultural Awareness in VR-based Simulations — Mascarenhas et al. (2019)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Forschungsprojekt |
| **Organisation** | INESC-ID / Universidade de Lisboa |
| **Branche** | HCI / Interkulturelles Training |
| **Region** | Portugal / Deutschland |
| **Link / Quelle** | Mascarenhas et al. (2019), *International Journal of Human-Computer Studies*, 126, 14–28 (QUELLE: mascarenhas2019cultural) |
| **Rolle von VR** | VR-Simulationen für interkulturelles Bewusstseinstraining; Avatare repräsentieren verschiedene Kulturen mit spezifischen Kommunikationsmustern |
| **Relevanz für P** | Offenheit (kulturelle Offenheit als Prädiktor der VR-Akzeptanz), Mentale Einschränkung (kulturell bedingte Technikskepsis), Alter |

**Beschreibung**: Mascarenhas et al. entwickeln VR-Crowd-Simulationen, in denen Avatare kulturell differenzierte Verhaltensweisen zeigen (Proxemik, Blickkontakt, Gesprächsrhythmus). Teilnehmer aus verschiedenen Kulturen erleben kulturell bekannte und fremde Verhaltensweisen in VR und geben Feedback zur Authentizität. Ergebnis: Kulturell kodierte Körpersprache wird auch in VR (über einfache Avatare) zuverlässig erkannt und löst kulturspezifische Reaktionen aus.

**Erkenntnisse für KMU**: Für KMU im deutsch-dänischen Grenzgebiet (geographischer Fokus des Projekts) oder mit internationalem Kundenstamm ist die Erkenntnis zentral: VR-Meetings sind nicht kulturell neutral. Avatarkörpersprache, Raumdistanzen und Kommunikationsrhythmen können kulturell missverstanden werden. *Offenheit* als Framework-Variable (Kap. 07) beschreibt nicht nur Technikoffenheit, sondern auch kulturelle Flexibilität — beides Prädiktoren erfolgreicher VR-Adoption in internationalen Teams.

---

**We Are Using the Wrong Assessment Metrics for VR — Langer et al. (2020)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Systematischer Review |
| **Organisation** | Deutsche Sporthochschule Köln |
| **Branche** | VR-Forschungsmethodologie |
| **Region** | Deutschland |
| **Link / Quelle** | Langer et al. (2020), *Virtual Reality*, 24(4), 611–623 (QUELLE: langer2020we) |
| **Rolle von VR** | Metastudie über Messinstrumente für VR-Wirkungen auf Körper und Wohlbefinden |
| **Relevanz für P** | Körperliche Ausprägungen (Motion Sickness, VR-Sickness), Technische Einschränkung (Headset-Komfort), Messmethodik |

**Beschreibung**: Neben seiner Relevanz für EU (→ Kap. 06) liefert dieser Review wichtige Erkenntnisse für die P-Domäne: Die häufigsten körperlichen Nebenwirkungen in VR-Studien sind Übelkeit (30–40 % der Stichproben), Schwindel (20–30 %) und Augenbelastung (40–60 %). Die Schwere variiert stark zwischen Personen und wird von Faktoren wie Geschlecht (Frauen tendenziell anfälliger), Alter (jüngere Nutzer adaptieren schneller) und Vorerfahrung (mit jeder Session sinkt Anfälligkeit) moderiert.

**Erkenntnisse für KMU**: *Körperliche Ausprägungen* sind kein Randthema — sie sind ein primärer Adoptionshemmschuh. Langer et al. empfehlen für Unternehmenseinsatz: Sitzende Bedienung statt stehend, Teleportation statt Locomotion, Session-Länge unter 30 Minuten für Erstnutzer, proaktives Monitoring. Für KMU bedeutet das konkret: Vor einem VR-Rollout sollte ein kurzes Screening der Belegschaft (FMS-Basismessung) eingeplant werden, um Hochrisikopersonen zu identifizieren und alternative Teilnahmeformate vorzubereiten.
