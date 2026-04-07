# Staging: Aufbereitete Fallstudien für Buch/04_anwendungsszenarien.md

> **Zweck:** Deduplizierte, kategorisierte und einheitlich formatierte Fallsammlung als Staging-Quelle für die Integration in `Buch/04_anwendungsszenarien.md`.
>
> **Deduplizierungshinweis:** Meyer Werft (Papenburg) ist bereits vollständig in `Kap. 04` aufgenommen — hier nicht nochmals einfügen. TeamViewer Frontline erschien im Ausgangsmaterial doppelt und wurde zu einem Eintrag zusammengeführt. Das MDZ Schleswig-Holstein erschien für zwei verschiedene Use Cases (Montageplanung + Digitaler Zwilling) — beide behalten, unter derselben Organisation.
>
> **Regionaler Fokus:** Norddeutsche und deutsche Fälle werden bevorzugt. Skandinavische Beispiele sind aufgenommen, wo ein direkter Branchenbezug zum deutsch-dänischen Grenzraum besteht. Internationale Fälle werden als Referenzpunkte geführt.

---

## Kategorie 1: Aus- und Weiterbildung / Training

*Mitarbeiterschulung, Sicherheitsunterweisung, Berufsausbildung, Onboarding*

---

**HellermannTyton GmbH & HAW Hamburg — VR-Modellierung von Maschinenrüstvorgängen (Tornesch, SH)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Praxisbeispiel / Hochschul-KMU-Kooperation |
| **Organisation** | HellermannTyton GmbH / HAW Hamburg (Projekt DigiNet.Air) |
| **Branche** | Kunststoffverarbeitung / Kabelmanagement |
| **Region** | Tornesch, Schleswig-Holstein / Hamburg |
| **Link / Quelle** | [HAW Hamburg – Mensch-Maschine-Kollaboration VR (PDF)](https://www.haw-hamburg.de/fileadmin/TI-MP/PDF/IPP-Sonstige_PDFs/B3_Mensch-Masch-Kollaboration-VR_2teOnlineKonferenz_HAW-Hamburg_Gutiq-Kastriote_20210112.pdf) |
| **Rolle von VR** | Übertragung realer Rüstprobleme in eine virtuelle Übungsumgebung — Mitarbeitende erlernen komplexe Maschinenrüstungen ohne Produktionsunterbrechung |
| **Relevanz für VA** | Meeting Type (Schulung/Kompetenzaufbau), VR-Eignung (komplexe Produktionsmaschinen sehr hoch), Anwendungsfall (Rüst- und Wartungstraining) |

**Was wurde gemacht?** Das produzierende KMU HellermannTyton (Kabelmanagement-Systeme) entwickelte gemeinsam mit der HAW Hamburg im Rahmen des Förderprojekts DigiNet.Air einen prototypischen VR-Ansatz für seine Maschinenrüstvorgänge. Reale Rüstprobleme aus der Produktion wurden als VR-Übungsszenarien nachgebaut. Mitarbeitende konnten Handgriffe, Abläufe und potenzielle Fehlerquellen in der virtuellen Umgebung trainieren und „durchdenken", bevor sie am echten Gerät arbeiten.

**Mehrwerte für KMU:**
- Keine Blockierung teurer Produktionsmaschinen für Trainingszeiten
- Fehler im Training kosten nichts — Fehler an der Anlage können Material und Zeit vernichten
- Kompetenzaufbau auch bei seltenen Rüstszenarien, die in der Praxis nur selten vorkommen
- Direktes SH-Beispiel: KMU aus Tornesch als Praxispartner einer Hamburger Hochschule — Kooperationsmodell übertragbar

**Herausforderungen:**
- Aufwändige 3D-Modellierung der Maschine als Grundlage — ohne CAD-Daten oder Laserscanning schwierig
- Prototypisch evaluiert; keine publizierten Wirksamkeitsdaten (Kompetenzgewinn nicht quantifiziert)
- Pflegeaufwand bei Maschinenänderungen (VR-Modell muss aktualisiert werden)

---

**Fraunhofer IML — XR-Lab: Gabelstapler-Simulatoren und Intralogistik-Training (Dortmund / Relevanz Hamburg/Bremen)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Angewandte Forschung / Transferangebot für KMU |
| **Organisation** | Fraunhofer-Institut für Materialfluss und Logistik (IML), XR Lab |
| **Branche** | Logistik / Intralogistik / Speditionswesen |
| **Region** | Dortmund (Forschungsstandort); Logistik-Hubs Hamburg, Bremen, Bremerhaven unmittelbar relevant |
| **Link / Quelle** | [Fraunhofer IML – XR Lab](https://www.iml.fraunhofer.de/de/unser-institut/forschungshallen-und-labore/xr-lab.html) |
| **Rolle von VR** | „Ready-to-Use"-Trainingsmodule für Warenannahme, Kommissionierung und Gabelstapler-Bedienung; Evaluation von Nutzerakzeptanz und Usability |
| **Relevanz für VA** | Anwendungsfall (Sicherheitstraining / Einarbeitung), VR-Eignung (gefährliche Umgebungen sehr hoch), Wahrgenommene Wirksamkeit |

**Was wurde gemacht?** Das XR Lab des Fraunhofer IML entwickelt und evaluiert VR/AR-Systeme für Logistik-KMU. Konkrete Angebote umfassen Gabelstapler-Simulatoren für das Anlernen neuer Mitarbeitender unter realistischen, aber sicheren Bedingungen sowie AR-gestützte Kommissionierhilfen („Pick-by-Vision"). Lösungen werden hinsichtlich Nutzerakzeptanz und Benutzerfreundlichkeit evaluiert — ein für KMU wichtiges Qualitätskriterium vor der Investitionsentscheidung.

**Mehrwerte für KMU:**
- Gabelstapler-Unfälle gehören zu den häufigsten Arbeitsunfällen in Lagerbetrieben — VR-Training reduziert dieses Risiko nachweislich
- Neue Mitarbeitende können produktiv eingesetzt werden, während das Simulator-Training läuft
- Fraunhofer als Transferpartner: KMU können Demonstratoren vor Ort erproben, bevor investiert wird
- AR-Kommissionierung (Pick-by-Vision) direkt kombinierbar mit VR-Training in einem Workflow

**Herausforderungen:**
- Entwicklungskosten für unternehmensindividuelle Lagerlayout-VR hoch; Fraunhofer-Lösungen sind noch nicht vollständig standardisiert
- Netzwerk-Latenz bei AR-Systemen in Echtzeit-Lagerumgebungen (Barcodes, WLAN-Dichte)

---

**TeamViewer Frontline — Industrie-Remote-Support und AR-gestützte Wartung (Bremen / Global)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Kommerzielle Software-Plattform (SaaS) |
| **Organisation** | TeamViewer AG (Göppingen; ehem. Ubimax, Bremen) |
| **Branche** | Industrie / Anlagenbau / Windenergie / Service |
| **Region** | Technologiebasis Bremen (Ubimax-Akquisition 2020); global eingesetzt |
| **Link / Quelle** | [TeamViewer Frontline](https://www.teamviewer.com/de/frontline/) |
| **Rolle von VR/AR** | Visuelle Fernunterstützung: Experte (z. B. in Hamburg) sieht das Live-Sichtfeld eines Technikers vor Ort (z. B. Windkraftanlage offshore) und kann Markierungen, 3D-Modelle und Schritt-für-Schritt-Anleitungen einblenden |
| **Relevanz für VA** | Meeting Type (Remote Support / Experten-Wissenstransfer), VR-Eignung (schwer zugängliche oder gefährliche Standorte sehr hoch), Anwendungsfall (Fernwartung) |

**Was wurde gemacht?** TeamViewer Frontline (entstanden aus der Ubimax-Akquisition 2020, Ursprung Bremen) ist eine kommerzielle AR/VR-Plattform für industriellen Remote Support. Ein Experte schaltet sich live auf die Headset-Perspektive eines Technikers vor Ort auf und kann Markierungen im Sichtfeld setzen sowie technische Zeichnungen einblenden. Eingesetzt wird das System u. a. für Reparaturen an Windkraftanlagen, Industriemaschinen und in der Automobilproduktion.

**Mehrwerte für KMU:**
- Drastische Reduktion von Reisekosten und Anreisezeiten für Servicespezialisten
- Kürzere Stillstandzeiten: Maschinenprobleme werden schneller diagnostiziert und behoben
- Kommerziell verfügbar, sofort einsetzbar — kein eigenes Entwicklungsprojekt nötig
- Besonders relevant für norddeutsche KMU mit Offshore-Servicegeschäft oder entlegenen Wartungsstandorten

**Herausforderungen:**
- Stabile Internetverbindung am Servicestandort zwingend (Offshore oder ländliche Standorte: Herausforderung)
- Datenschutz: Live-Videostream enthält ggf. schutzbedürftige Produktionsdaten
- Schulungsaufwand für Außendiensttechniker, die die AR-Brille bedienen sollen

---

**Vestas Wind Systems / VRAI — Offshore-Sicherheitstraining in VR (Dänemark)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Industrie-Pilotprojekt / Kooperation Startup + Großkonzern |
| **Organisation** | Vestas Wind Systems A/S (Partner: VRAI, Port of Blyth Training Services) |
| **Branche** | Offshore-Windenergie |
| **Region** | Dänemark (direkte Relevanz für SH/Niedersachsen als Offshore-Windstandorte) |
| **Link / Quelle** | [OWGP: VRAI Case Study](https://owgp.org.uk/case-studies/vrai/); [Vestas VR Storytelling auf Messen](https://cadpeople.com/cases/veastas-vr-storytelling/) |
| **Rolle von VR** | (a) Portables Sicherheitstraining für Brandschutz und Notfallszenarien unter simulierten Offshore-Bedingungen; (b) Immersive B2B-Messepräsentation: Drohneninspektion eines 61-m-Rotorblatts aus 140 m Höhe erlebbar |
| **Relevanz für VA** | Anwendungsfall (Sicherheitstraining / B2B-Marketing), VR-Eignung (gefährliche/unzugängliche Umgebungen sehr hoch) |

**Was wurde gemacht?** (a) Vestas entwickelte gemeinsam mit dem Startup VRAI ein portables VR-Brandschutztraining speziell für Offshore-Techniker. Das Modul bildet reale Offshore-Bedingungen nach (enge Räume, Geräusch, Seegang) und schult sicherheitskritische Abläufe ohne Blockierung echter Anlagen. Portabilität: Das System kann an Schulungszentren weltweit eingesetzt werden. (b) Auf Messen setzt Vestas VR ein, um komplexe Sachverhalte zugänglich zu machen — Besucher erleben simulierte Drohneninspektionen und Errichterschiff-Boarding.

**Mehrwerte für KMU:**
- Schulung in Extremszenarien (Brand offshore), die real nicht trainierbar sind
- Globale Skalierbarkeit: Techniker in SH, Niedersachsen und Dänemark trainieren mit denselben Inhalten
- Messe-VR als differenzierender Vertriebskanal auch für mittelständische Windenergie-Zulieferer übertragbar

**Herausforderungen:**
- Entwicklungspartnerschaft mit Startup erforderlich — nicht Off-the-Shelf
- Zertifizierungsanerkennung: ob VR-Training bestehende Präsenzpflicht in Sicherheitsschulungen ersetzt, ist regulatorisch zu klären (variiert je nach Zertifizierungsstelle)

---

**Mittelstand-Digital Zentrum Hamburg — VR für Onboarding und Indoor-Navigation**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Best Practice / Umsetzungsprojekt für KMU |
| **Organisation** | Mittelstand-Digital Zentrum Hamburg |
| **Branche** | Branchenübergreifend (Handwerk, Verwaltung, Dienstleistung) |
| **Region** | Hamburg |
| **Link / Quelle** | [Digitalzentrum Hamburg: Praxisbeispiele Handwerksbetriebe](https://digitalzentrum-hamburg.de/category/handwerksbetrieben/) |
| **Rolle von VR** | Ortsgebundene, visuelle Navigation durch Bürokomplexe und Betriebsgebäude für neue Mitarbeitende und externe Gäste |
| **Relevanz für VA** | Anwendungsfall (Onboarding), VR-Eignung (räumliche Orientierung / Gebäudekenntnisse), Meeting Type (Einführung/Einweisung) |

**Was wurde gemacht?** Das Mittelstand-Digital Zentrum Hamburg dokumentierte und begleitete einen Use Case, in dem VR zur effizienten Einführung neuer Mitarbeitender und externer Gäste in komplexe Büro- oder Betriebsgebäude eingesetzt wurde. Anwender erhalten ortsgebunden relevante Informationen zur Ausstattung und internen Organisation — ohne personalintensive Führungen.

**Mehrwerte für KMU:**
- Reduzierter Organisationsaufwand bei Einarbeitungen (keine Führungen durch Kollegen nötig)
- Jederzeit abrufbar, wiederholbar und skalierbar (z. B. für Saisonkräfte)
- Niedrigschwellige Einstiegslösung: VR-Onboarding kann mit 360°-Touren begonnen werden

**Herausforderungen:**
- Pflege der VR-Umgebung bei Raumveränderungen
- Für sehr kleine Betriebe (<10 MA) ist ROI gering

---

## Kategorie 2: Fabrik- & Arbeitsplatzplanung

*Montageplanung, Ergonomieoptimierung, Shopfloor-Management, digitale Fabrik*

---

**Mittelstand-Digital Zentrum Schleswig-Holstein — VR in der Montageplanung**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Transferprojekt / Demonstratorangebot für KMU |
| **Organisation** | Mittelstand-Digital Zentrum Schleswig-Holstein |
| **Branche** | Produktion / Maschinenbau / Handwerk |
| **Region** | Schleswig-Holstein |
| **Link / Quelle** | [Demonstratoren MDZ Schleswig-Holstein](https://www.digitalzentrum-sh.de/demonstratoren) |
| **Rolle von VR** | Eigenständige Montageplanung: Unternehmen erproben virtuell Anpassungen am Shopfloor, bevor reale Maschinen umgestellt oder Umbaumaßnahmen eingeleitet werden |
| **Relevanz für VA** | Anwendungsfall (Fabrikplanung / Layoutoptimierung), VR-Eignung (räumliche Planung sehr hoch), KMU-spezifisch (Demonstratoren zur Eigennutzung) |

**Was wurde gemacht?** Das MDZ Schleswig-Holstein stellt regionalen KMU VR-Demonstratoren zur eigenständigen Erprobung bereit. Im Bereich Montageplanung können Betriebe Shopfloor-Layouts virtuell testen — Laufwege, Maschinenpositionierungen und Materialflüsse werden in 3D erlebbar, bevor kostenspielige physische Umbauten stattfinden. Die Nutzung der Demonstratoren ist für SH-KMU kostenlos.

**Mehrwerte für KMU:**
- Kostenloser Einstieg ohne Eigentinvestition (Demonstratornutzung via MDZ)
- Fehler in der Planung werden vor dem Umbau sichtbar — nicht danach
- Direkter regionaler Ansprechpartner für SH-KMU; niedrigschwelliger Transfer

**Herausforderungen:**
- Datenaufbereitung (3D-Modelle von Maschinen und Halle) erfordert Vorbereitung durch das Unternehmen
- Individualisierung über Standard-Demonstratoren hinaus erfordert Dienstleistereinsatz

---

**Halocline GmbH — VR-Montageplanung ohne CAD-Kenntnisse (Osnabrück, Niedersachsen)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Marktreifes Softwareprodukt (SaaS) |
| **Organisation** | Halocline GmbH |
| **Branche** | Produktionsplanung / Fertigungsindustrie |
| **Region** | Osnabrück, Niedersachsen |
| **Link / Quelle** | [Halocline – VR in der Produktion](https://halocline.io/anwendungsbereiche/) |
| **Rolle von VR** | Prozessplaner bauen Montagearbeitsplätze virtuell nach und validieren sofort Ergonomie, Laufwege und Griffbereiche — ohne CAD-Vorkenntnisse |
| **Relevanz für VA** | Anwendungsfall (Ergonomie / Arbeitsplatzgestaltung), VR-Eignung (komplexe räumliche Planungsaufgaben sehr hoch), Marktprodukt direkt einsetzbar |

**Was wurde gemacht?** Halocline bietet eine SaaS-VR-Plattform speziell für mittelständische Fertigungsbetriebe: Prozessplaner ohne CAD-Kenntnisse können darin Arbeitsplätze „zusammenbauen" und sofort ergonomisch testen. Laufwege, Griffbereiche und Maschinenzugänglichkeit werden vor der physischen Realisierung erlebbar gemacht. Das Produkt ist kommerziell verfügbar und direkt einsetzbar.

**Mehrwerte für KMU:**
- Kein CAD-Know-how nötig — Planung durch Meister und Prozessplaner direkt möglich
- Frühe Ergonomie-Validierung reduziert spätere Arbeitsunfälle und Anpassungskosten
- SaaS-Modell: keine eigene Server-Infrastruktur

**Herausforderungen:**
- Integration der VR-Planungsdaten zurück in bestehende ERP/PLM-Systeme noch aufwändig
- Datenbank von Maschinen und Betriebsmitteln muss gepflegt und erweitert werden

---

**Digital Reality Academy / VW Group Academy — VR-Shopfloor-Management für den Mittelstand (Hannover)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Transfer-Hub für Mittelstands-Netzwerke |
| **Organisation** | VW Group Academy / Deutsche Messe Technology Academy |
| **Branche** | Fertigungsindustrie / Management |
| **Region** | Hannover, Niedersachsen |
| **Link / Quelle** | [Digital Reality Academy Hannover](https://www.technology-academy.group/partner-digital-reality-academy/) |
| **Rolle von VR** | Live-Erprobung von Design-Reviews, Shopfloor-Meetings und abteilungsübergreifenden Planungen; Transfer von Großserienkonzepten (VW) in den Mittelstand |
| **Relevanz für VA** | Meeting Type (Design Review / Shopfloor-Meeting), Anwendungsfall (Wissenstransfer Großunternehmen → KMU), VR-Eignung (Planungsprozesse) |

**Was wurde gemacht?** Die Digital Reality Academy in Hannover dient als physischer Erprobungsort, an dem KMU-Partner VR- und AR-Technologien dauerhaft in ihre Workflows integrieren lernen. Nicht rein technische Schulung steht im Fokus, sondern die Anwendung von VR für Shopfloor-Management und abteilungsübergreifende Design-Reviews. Praxisnahe Use Cases aus der Großserie (VW) werden gezielt für den Mittelstand adaptiert und dokumentiert.

**Mehrwerte für KMU:**
- Erprobungsinfrastruktur ohne Eigeninvestition nutzbar
- Wissenstransfer aus der Automobilindustrie: bewährte Prozesse für VR-gestütztes Management übertragbar
- Netzwerkeffekt: KMU-Netzwerke können gemeinsam Use Cases entwickeln

**Herausforderungen:**
- Fokus auf Fertigungsindustrie; für Dienstleistungs-KMU weniger direkt relevant
- Räumliche Nähe zu Hannover erforderlich für Präsenzveranstaltungen

---

**Hochschule Koblenz — VR-Optimierung von Blechfertigung und Montageplatz-Ergonomie**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Case Study / Angewandte Forschung |
| **Organisation** | Hochschule Koblenz |
| **Branche** | Maschinenbau / Produktionstechnik |
| **Region** | Rheinland-Pfalz (Methodik auf deutschen Mittelstand übertragbar) |
| **Link / Quelle** | [Pressemitteilung Hochschule Koblenz](https://www.hs-koblenz.de/rmc/aktuelles/presse/detail/_n/virtual-reality-in-produktion-und-logistik-case-study-der-hochschule-koblenz-zeigt-vorteile-der-technologie) |
| **Rolle von VR** | Immersive 3D-Darstellung einer Blechfertigung; virtuelle Simulation von Bewegungsabläufen an Montagearbeitsplätzen zur Ergonomie- und Produktivitätsoptimierung |
| **Relevanz für VA** | Anwendungsfall (Fabrikplanung / Ergonomie), VR-Eignung (räumliche Produktionsplanungsaufgaben sehr hoch) |

**Was wurde gemacht?** Eine Case Study der Hochschule Koblenz belegt, wie VR-Engines genutzt werden können, um Optimierungspotenziale in Produktionsbetrieben frühzeitig sichtbar zu machen. Durch virtuelle Rundgänge in einer 3D-Blechfertigung werden Planungsentscheidungen direkt erlebbar. Ergänzend werden Gegenstände und Bewegungsabläufe an Montageplätzen virtuell nachgestellt und unter Ergonomie- und Effizienzgesichtspunkten bewertet.

**Mehrwerte für KMU:** Dokumentierte Methodik für KMU ohne eigene VR-Kompetenz; zeigt Schritt-für-Schritt, wie bestehende Fertigungslayouts digitalisiert und in VR überführt werden.

**Herausforderungen:** Hochschulstudie; keine publizierten ROI-Zahlen aus Praxisbetrieben.

---

**Krones AG — Kollaborativer Design Review für Getränkeabfüllanlagen**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Unternehmensimplementierung (Engineering-Tool) |
| **Organisation** | Krones AG (Maschinen- und Anlagenbau) |
| **Branche** | Anlagenbau / Getränkeindustrie |
| **Region** | Bayern (relevante Kunden im norddeutschen Brauereibereich) |
| **Link / Quelle** | [Krones – Virtual Reality in der Anlagenplanung](https://www.krones.com/de/unternehmen/digitalisierung.php) |
| **Rolle von VR** | Ingenieure und Kunden treffen sich als Avatare im VR-Modell einer kompletten Abfülllinie; Kollisionen und Wartungsengpässe werden erkannt, bevor die Anlage gebaut wird |
| **Relevanz für VA** | Meeting Type (Remote Collaboration / Design Review), VR-Eignung (komplexe Anlagengeometrien sehr hoch) |

**Was wurde gemacht?** Krones nutzt VR für kollaborative Design-Reviews mit Kunden und internen Ingenieuren: In virtuellen Walkthrough-Sitzungen wird die gesamte Abfülllinie begangen. Kollisionen zwischen Rohrleitungen, unzureichende Wartungszugänglichkeit oder Schnittstellenprobleme werden im VR-Modell identifiziert und direkt besprochen — bevor das erste Bauteil gefertigt wird.

**Mehrwerte für KMU:** Template für KMU-Zulieferer des Anlagenbaus: Wer seinen Kunden virtuelle Anlagen-Reviews anbieten kann, differenziert sich im Wettbewerb. Besonders relevant für norddeutsche Brauereizulieferer.

**Herausforderungen:** Multi-User-Synchronisation bei großen CAD-Datenmengen rechenintensiv; stabile Verbindungen aller Teilnehmer erforderlich.

---

## Kategorie 3: Virtual Prototyping & kollaborative Design-Reviews

*Produktentwicklung, Bemusterung, Digitaler Zwilling als Design-Instrument*

> **Hinweis:** Meyer Werft (Papenburg) ist bereits vollständig in `Buch/04_anwendungsszenarien.md` aufgenommen. Nicht nochmals einfügen.

---

**Drägerwerk AG — VR-basiertes Participatory Design für Krankenhaus-Arbeitsplätze (Lübeck, SH)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Unternehmensimplementierung (Realitätsnahes Prototyping) |
| **Organisation** | Drägerwerk AG & Co. KGaA, Design Center |
| **Branche** | Medizintechnik / Krankenhausplanung |
| **Region** | Lübeck, Schleswig-Holstein |
| **Link / Quelle** | [Dräger Design Center (PDF)](https://www.draeger.com/Content/Documents/Newsroom/Draeger-Design-Center-Die-Klinik-von-morgen-schon-heute-erlebbar-machen.pdf) |
| **Rolle von VR** | „Mini-Krankenhaus" zur immersiven 3D-Planung und ergonomischen Validierung zukünftiger OP-Säle und Intensivstationen vor dem Bau |
| **Relevanz für VA** | Anwendungsfall (Virtual Prototyping / Workspace Design), Meeting Type (Co-Creation / Planungsbesprechung), VR-Eignung (komplexe räumliche Planung sehr hoch) |

**Was wurde gemacht?** Das Dräger Design Center in Lübeck nutzt VR-Simulationen, um teure Planungsfehler bei der Gestaltung von Krankenhäusern zu vermeiden. Architekten, Klinikplaner und das spätere medizinische Fachpersonal (Ärzte, Pflegekräfte) begehen geplante OP-Säle und Intensivstationen immersiv, bevor ein Stein gesetzt ist. Arbeitsabläufe, Gerätepositionierungen und Lichtverhältnisse werden gemeinsam getestet und angepasst (Participatory Design).

**Mehrwerte für KMU:**
- Kostensenkung durch Vermeidung nachträglicher baulicher Änderungen (Änderungen auf dem Papier vs. im fertigen Bau sind um Größenordnungen günstiger)
- Einbindung der Endanwender erhöht Prozesssicherheit und Akzeptanz des neuen Arbeitsplatzes drastisch
- **KMU-Transfer:** Direkt anwendbar für norddeutsche Anlagenbauer, Intralogistik-Planer und Architekten, bei denen Kunden-Co-Creation in der Planungsphase entscheidend ist

**Herausforderungen:**
- Hochwertige VR-Infrastruktur (Tracking-Room) nötig; nicht ad-hoc replizierbar
- Anforderungsmanagement: Medizintechnik-Kontext mit strengen regulatorischen Anforderungen — für andere Branchen einfacher umsetzbar

---

**Team Malizia & VRtual X — Digitaler Zwilling im maritimen Yachtbau (Hamburg)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Entwicklungskooperation / Praxiseinsatz |
| **Organisation** | Team Malizia (Boris Herrmann Racing) in Kooperation mit PICO und VRtual X (Hamburg) |
| **Branche** | Maritime Industrie / Bootsbau / Hochleistungssport |
| **Region** | Hamburg |
| **Link / Quelle** | [Sail-World Report (2022)](https://www.sail-world.com/news/256751/Team-Malizia-designed-with-PICO-and-VRtual-X) |
| **Rolle von VR** | Vollständiges ergonomisches Design und Validierung der IMOCA60-Rennyacht „Malizia – Seaexplorer" als Digitaler Zwilling vor der Fertigung |
| **Relevanz für VA** | Anwendungsfall (Digitaler Zwilling / Virtual Prototyping), VR-Eignung (räumlich eng begrenzte, ressourcenkritische Designs sehr hoch) |

**Was wurde gemacht?** Das Hamburger Team entwickelte die Offshore-Rennyacht von Beginn an im VR-Modell. Die Segelcrew konnte das enge Cockpit immersiv „begehen" und kritische Handgriffe, Sichtachsen und die Ergonomie unter simulierten Bedingungen testen — ohne teure physische Holz-Mock-ups. VR ersetzte den vollständigen Mock-up-Prozess, der bei einer Hochleistungsyacht mehrere zehntausend Euro kostet.

**Mehrwerte für KMU:**
- Drastische Material- und Ressourceneinsparung beim Prototypenbau
- Iterative, sofort testbare Ergonomieanpassung in der Planungsphase
- **KMU-Transfer:** Hochgradig übertragbar auf Bootsbauer, Sonderfahrzeughersteller, Wohnmobilbauer und Anhänger-KMU in Norddeutschland, bei denen „Packaging" (optimale Raumnutzung) entscheidend ist

**Herausforderungen:**
- Kooperation mit spezialisierter VR-Agentur (VRtual X) erforderlich
- Für Massenprodukte mit vielen Varianten ist der Individualisierungsaufwand hoch

---

**Lufthansa Technik AG — VR-Konfiguration von VIP-Flugzeugkabinen (Hamburg)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Unternehmensimplementierung / B2B-Vertriebs- und Design-Tool |
| **Organisation** | Lufthansa Technik AG |
| **Branche** | Luftfahrt / Wartung & Kabinen-Design |
| **Region** | Hamburg (Completion Center) |
| **Link / Quelle** | [Lufthansa Technik – Cabin Design Center](https://www.lufthansa-technik.com/de/cabin-design-center) |
| **Rolle von VR** | Potenzielle VIP-Jet-Käufer konfigurieren Kabinenausstattungen (Materialien, Layouts, Lichtstimmungen) in Echtzeit in VR — primäres Vertriebswerkzeug im Hochpreissegment |
| **Relevanz für VA** | Meeting Type (B2B-Vertrieb / Produktkonfiguration), VR-Eignung (hochwertige Materialdarstellung und individuelle Kundenerfahrung sehr hoch) |

**Was wurde gemacht?** Im Hamburger Completion Center setzt Lufthansa Technik VR als primäres Verkaufsinstrument für die Individualkonfiguration von Privatjet-Innenräumen ein. Kunden erleben Ledertexturen, Holzfurniere, Leuchtkonzepte und Raumlayouts in Echtzeit und können unmittelbar Änderungen anfordern — in einer virtuellen Kabine statt in aufwändigen physischen Musterräumen.

**Mehrwerte für KMU:**
- **KMU-Transfer:** Direktes Modell für Schiffsinnenausstatter, Wohnmobilhersteller oder Sonderfahrzeug-KMU: VR als Konfigurationstool ersetzt teure Musterwände und Showrooms
- Höhere Abschlussquote durch emotionale Erlebbarkeit vor der Kaufentscheidung
- Reduzierung von Nachbearbeitungen, da Kundenwünsche vorab geklärt sind

**Herausforderungen:**
- Fotorealistisches Rendering von Premiumaterialien (Leder, Edelholz) technisch anspruchsvoll
- Laufende Pflege der Materialdatenbank

---

**Airbus — RealityWorks & Kabinen-Design-Reviews (Hamburg)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Inhouse-Entwicklungstool (Großkonzern) |
| **Organisation** | Airbus SE |
| **Branche** | Luftfahrt / Flugzeugbau |
| **Region** | Hamburg-Finkenwerder |
| **Link / Quelle** | [Airbus VR Innovation](https://www.airbus.com/en/innovation/tech-and-digital/virtual-and-augmented-reality) |
| **Rolle von VR** | Kollaboratives 3D-Skizzieren und Validieren von Kabinenkomponenten; Kabineninspektion tausender Bauteile am Rumpf |
| **Relevanz für VA** | Anwendungsfall (Design Review / Qualitätskontrolle), Zeitersparnis bei komplexen Inspektionsprozessen |

**Was wurde gemacht?** Airbus nutzt VR in Hamburg als „3D-Sketching-Board" für Kabinen-Layouts: Designer entwerfen in VR, Kunden können auf echten Sitzen Platz nehmen und dabei die virtuelle Kabinenumgebung erleben. Inspektionszeiten für Tausende Bauteile am Rumpf sanken laut Airbus von Wochen auf Tage.

**Mehrwerte für KMU:** Zeigt das Skalierungspotenzial: Was bei Airbus Wochen spart, spart bei KMU-Zulieferern ebenfalls proportional Zeit. Hamburger Standort: direkter regionaler Relevanznachweis für norddeutsche Luftfahrtzulieferer.

**Herausforderungen:** Airbus-interne Lösung; nicht direkt kommerziell verfügbar. Vergleichbare SaaS-Lösungen: Hololight (s. u.), Scope AR.

---

**Hololight — Industrielles CAD-Streaming für Design-Reviews (München)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Kommerzielle Softwarelösung (Hololight Hub) |
| **Organisation** | Hololight GmbH |
| **Branche** | Maschinenbau / Anlagenbau / Engineering |
| **Region** | Ismaning/München (deutschlandweit einsetzbar) |
| **Link / Quelle** | [Hololight Hub](https://hololight.com/) |
| **Rolle von VR** | Streaming sehr großer CAD-Datenmengen auf VR-Headsets in Originalqualität — gemeinsame Design-Reviews am digitalen Zwilling in Originalgröße |
| **Relevanz für VA** | Anwendungsfall (kollaborativer Design Review), VR-Eignung (große CAD-Datensätze ohne Qualitätsverlust sehr hoch) |

**Was wurde gemacht?** Hololight Hub streamt hochkomplexe CAD-Modelle (wie sie in Maschinenbau und Anlagenbau entstehen) auf VR-Headsets, ohne die Datenmenge zu reduzieren. Mehrere Ingenieure können gleichzeitig am originalen digitalen Zwilling arbeiten, Bauteile prüfen und Änderungen direkt validieren — ohne physische Mock-ups.

**Mehrwerte für KMU:** Deutsches Produkt, auf KMU-Engineering ausgerichtet; keine Reduktion der Modellqualität; SaaS-Modell verfügbar. Besonders relevant für norddeutsche Maschinenbau-KMU mit internationalen Kunden, die Design Reviews ortsunabhängig durchführen wollen.

**Herausforderungen:** Stabile, schnelle Internetverbindung am Standort aller Teilnehmer erforderlich (Cloud-Streaming).

---

**Volvo Cars & Unity — Echtzeit-3D für abteilungsübergreifende Produktentwicklung (Schweden)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Unternehmensimplementierung / Case Study (international) |
| **Organisation** | Volvo Cars in Kooperation mit Unity Technologies |
| **Branche** | Automobilindustrie |
| **Region** | Göteborg, Schweden (Referenzfall für skandinavische Industrie) |
| **Link / Quelle** | [Unity Case Study: Volvo Cars](https://unity.com/resources/volvo) |
| **Rolle von VR** | CAD-Daten (CATIA, NX) werden direkt in fotorealistische VR-Umgebungen überführt; Ingenieure und Designer begehen denselben virtuellen Prototypen abteilungsübergreifend |
| **Relevanz für VA** | Anwendungsfall (Virtual Prototyping), VR-Eignung (komplexe Produkte mit vielen Varianten sehr hoch) |

**Was wurde gemacht?** Volvo nutzt Unity als Echtzeit-3D-Brücke zwischen CAD-Abteilung und Design- sowie Management-Teams: Statt Präsentationsfolien werden Fahrzeugeigenschaften direkt immersiv demonstriert. Management-Entscheidungen über Designdetails können an einem virtuellen Fahrzeug-Prototypen getroffen werden.

**Mehrwerte für KMU:** Zeigt das Potenzial für den norddeutschen Automobilzulieferer-Bereich: Wer CAD-Daten hat, kann sie mit Unity oder vergleichbaren Tools (Unreal, Hololight) kostengünstig in VR überführen und Kunden-Reviews virtuell abhalten.

**Herausforderungen:** Großkonzern-Implementierung mit eigenem IT-Team; KMU benötigen Dienstleister oder SaaS-Lösung. Lizenzkosten für Unity-Enterprise-Tier prüfen.

---

**KONE Corporation & Tampere University — Multi-User-VR für Aufzugsplanung (Finnland)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Angewandte Forschung / Industrie-Pilotprojekt (peer-reviewed) |
| **Organisation** | KONE Corporation in Kooperation mit Tampere University |
| **Branche** | Anlagenbau / Aufzugtechnik |
| **Region** | Finnland (Pilotprojekte in USA, Dubai, Malaysia) |
| **Link / Quelle** | [MDPI – Remote Collaboration in Construction](https://www.mdpi.com/2079-9292/10/22/2806) |
| **Rolle von VR** | Fernkollaboration zur Planung von Maschinenräumen für Hochhausaufzüge; asynchrone Wartungsplanung und kollaborative Risikobewertung |
| **Relevanz für VA** | Meeting Type (Remote Collaboration / Risikobewertung), VR-Eignung (Raumplanung / Instandhaltungsplanung sehr hoch) |

**Was wurde gemacht?** KONE erprobte Multi-User-VR zur Planung von Aufzugs-Maschinenräumen in realen Bauprojekten. Ingenieure aus verschiedenen Ländern trafen sich als Avatare im gleichen virtuellen Raum und konnten auf Bauteile zeigen, nonverbale Hinweise geben und gemeinsam Risikobewertungen durchführen. Eine Folgestudie untersuchte die kollaborative Prüfung technischer Wartungsdokumentationen in VR.

**Mehrwerte für KMU:** Peer-reviewed belegt, dass VR nonverbale Koordination bei Remote-Teams ermöglicht, die über reine Video-Calls nicht möglich ist. Template für Instandhaltungsplanung im KMU-Anlagenbau.

**Herausforderungen:** Aktuelle Avatare übertragen Mimik noch unzureichend — laut Studie beeinträchtigt dies die wahrgenommene soziale Präsenz (vgl. auch Moser et al. 2020).

---

## Kategorie 4: Fernwartung & Remote Support

*Remote Inspection, Troubleshooting, Experten-Support über Distanz*

---

**Mittelstand-Digital Zentren Bremen & Hamburg — AR/VR-Assistenzsysteme für maritime Wartung**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Demonstratorprojekt für KMU (Mittelstand-Digital) |
| **Organisation** | Mittelstand-Digital Zentren Bremen und Hamburg (Elbcampus) |
| **Branche** | Maritime Wirtschaft / Offshore-Windenergie / Wartung |
| **Region** | Norddeutschland (Bremen, Hamburg) |
| **Link / Quelle** | [Mittelstand-Digital – Elbcampus Veranstaltung](https://www.mittelstand-digital.de/MD/Redaktion/DE/TERMIN-IMPORT/2023/1672137831843-7165-Termin.html) |
| **Rolle von VR/AR** | (a) „Flüssiggas-Armaturen-Assistenzsystem": AR-geführte Wartung von Armaturensets bei Schiff-zu-Schiff-LNG-Transfer; (b) Fehlerfreie Instandhaltung von Windenergieanlagen via AR-Führung am Objekt |
| **Relevanz für VA** | Anwendungsfall (Wartung kritischer Infrastruktur), VR/AR-Eignung (gefährliche Umgebungen / seltene Vorgänge sehr hoch) |

**Was wurde gemacht?** Die norddeutschen Mittelstand-Digital Zentren entwickelten praxisnahe Demonstratoren speziell für maritime KMU und Windenergie-Servicebetriebe. Das Flüssiggas-Armaturen-System führt Techniker visuell durch sicherheitskritische Wartungsschritte beim Schiff-zu-Schiff-LNG-Transfer. Ein weiteres System unterstützt Servicetechniker an Windenergieanlagen mit schritt-weisen AR-Anleitungen direkt am Objekt — Sicherheit und Fehlerfreiheit werden erhöht.

**Mehrwerte für KMU:**
- Direkte Norddeutschland-Relevanz: maritime Branche und Offshore-Wind sind Kernbranchen der Region
- Demonstratoren kostenlos nutzbar (geförderte Zentren)
- Sicherheitsrelevanz: Fehler bei LNG-Transfer oder Windanlagen-Wartung haben fatale Folgen — VR/AR senkt das Risiko messbar

**Herausforderungen:** Standortbasierte Verfügbarkeit der Demonstratoren; für individuelle Unternehmensprozesse Anpassungsaufwand.

---

**Fette Compacting GmbH — VR-Troubleshooting unter Reinraumbedingungen via Avatar (Schwarzenbek, SH)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Unternehmensimplementierung (Fehlerprävention) |
| **Organisation** | Fette Compacting GmbH |
| **Branche** | Maschinen- und Anlagenbau (Pharmaindustrie) |
| **Region** | Schwarzenbek, Schleswig-Holstein (Metropolregion Hamburg) |
| **Link / Quelle** | [Prozesstechnik Online – Avatar Helmut hilft (2020)](https://prozesstechnik.industrie.de/partner/avatar-helmut-hilft/) |
| **Rolle von VR** | Training kritischer Rüst- und Reinigungsprozesse an Pharma-Isolatoren via VR-Avatar; der Avatar basiert auf einem realen langjährigen Unternehmensexperten |
| **Relevanz für VA** | Anwendungsfall (Wartung / Troubleshooting), Meeting Type (Experten-Wissenstransfer), VR-Eignung (hochverfügbare Maschinen / Reinraum sehr hoch) |

**Was wurde gemacht?** Der SH-Maschinenbauer Fette Compacting identifizierte, dass rund die Hälfte aller Fehler in der Pharmaproduktion durch mangelhaft geschultes Personal bei Rüst- und Reinigungsprozessen entsteht. Ein VR-Szenario wurde entwickelt, in dem Mitarbeitende komplexe Handschuheingriffe zur Reinigung eines Isolators üben können. Ein fachkundiger Avatar „Helmut" — modelliert auf Basis eines realen Unternehmensexperten — führt durch den Prozess.

**Mehrwerte für KMU:**
- Hochpreisige Maschinen (Millionenbereich) werden nicht für Trainings blockiert — Produktion läuft parallel
- Risikofreies Üben von Prozessen, bei denen echte Fehler ganze Produktchargen kontaminieren würden
- **Expertenwissen-Transfer:** Das Modell „Avatar als digitaler Experte" sichert Fachwissen eines erfahrenen Mitarbeitenden und macht es skalierbar verfügbar
- **KMU-Transfer:** Alle KMU mit teuren, empfindlichen Maschinen und komplexen Einrüstprozessen profitieren von diesem Modell (Lebensmittelproduktion, Feinmechanik, Pharmakonfektionierung)

**Herausforderungen:**
- Aufwand für 3D-Modellierung der Maschine und Animation der Handgriffe hoch (Initialinvestition)
- Avatar-Erstellung und Dialogsystem erfordern Expertise; laufende Pflege bei Prozessänderungen

---

**SMS Group — Remote Site Management und virtuelle Bauabnahmen im Anlagenbau**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Projektbezogener Praxiseinsatz (Großkonzern) |
| **Organisation** | SMS Group GmbH |
| **Branche** | Anlagenbau (Stahl, Metallindustrie) |
| **Region** | Düsseldorf (international tätig; Referenz für norddeutsche Anlagenbauer) |
| **Link / Quelle** | [SMS Group – Digitalisierung & VR](https://www.sms-group.com/de/technologien/digitalisierung) |
| **Rolle von VR** | Virtuelle Baustellenbegehungen und Planungsbesprechungen trotz Reisebeschränkungen; digitale Bauabnahmen aus der Ferne |
| **Relevanz für VA** | Meeting Type (Remote Projekt-Meeting / Bauabnahme), VR-Eignung (ortsunabhängige Projektkoordination sehr hoch) |

**Was wurde gemacht?** Bei internationalen Anlagenprojekten (u. a. Gasometer-Bau in Russland während Reisebeschränkungen) nutzte die SMS Group VR-Brillen für virtuelle Baustellenbegehungen. Ingenieure in Deutschland konnten Baufortschritte prüfen und Planungsdetails direkt am virtuellen Modell besprechen — Reise entfiel komplett.

**Mehrwerte für KMU:** Template für norddeutsche Anlagenbauer mit internationalen Projekten: VR-Meetings als Standard für Zwischenabnahmen und Baufortschritts-Reviews spart erhebliche Reisekosten.

**Herausforderungen:** Qualität der virtuellen Bauabnahme hängt von der Aktualität des 3D-Modells ab (As-built vs. As-planned Divergenz ist ein bekanntes Problem).

---

## Kategorie 5: B2B-Vertrieb, Marketing & virtuelle Showrooms

*Virtuelle Werksführungen, Produktpräsentationen, immersive Messeerlebnisse*

---

**Jungheinrich AG — Virtueller Showroom für automatisierte Lagersysteme (Hamburg)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Globales Vertriebstool |
| **Organisation** | Jungheinrich AG |
| **Branche** | Intralogistik / Lagertechnik |
| **Region** | Hamburg (Hauptsitz) |
| **Link / Quelle** | [Jungheinrich – Virtual Reality Showroom](https://www.jungheinrich.com/de/loesungen/digitale-loesungen/virtual-reality-showroom-825506) |
| **Rolle von VR** | Hochkomplexe Automatisierungslösungen (Regalbediengeräte, fahrerlose Transportsysteme) werden auf Messen und beim Kunden vor Ort in VR begehbar gemacht — da der physische Showroom nicht zum Kunden gebracht werden kann |
| **Relevanz für VA** | Meeting Type (Vertriebspräsentation / Kundenberatung), VR-Eignung (räumlich großskalige Produkte sehr hoch) |

**Was wurde gemacht?** Jungheinrich (Hamburg) setzt VR-Headsets im B2B-Vertrieb ein, um komplette automatisierte Logistikzentren erlebbar zu machen — eine Anlage, die eine Halle füllt, lässt sich physisch nicht demonstrieren. Vertriebsmitarbeitende führen Kunden auf Messen oder beim Kunden vor Ort durch virtuelle Logistikzentren.

**Mehrwerte für KMU:**
- Hamburger Best Practice: lokal verifizierbares Unternehmen
- Template für alle KMU, die großskalige oder standortgebundene Produkte/Dienstleistungen vertreiben (Maschinen, Anlagen, Gebäudelösungen)
- Vertrieb ohne Showroom-Infrastruktur: VR ersetzt teure Ausstellungsfläche

**Herausforderungen:** Schulung des Vertriebsaußendienstes für souveränen VR-Einsatz vor Ort; technischer Support nötig.

---

**enra GmbH — Virtuelle Werksführungen im produzierenden Mittelstand**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Technologischer Leitfaden / Use-Case-Dokumentation |
| **Organisation** | enra GmbH (B2B Sales Software) |
| **Branche** | Maschinenbau / Produzierendes Gewerbe |
| **Region** | Deutschlandweit für den Mittelstand anwendbar |
| **Link / Quelle** | [enra Blog: Virtuelle Werksführung](https://blog.enra.app/virtuelle-werksfuhrung/) |
| **Rolle von VR** | Digitale und immersive Nachbildung von Fabrikhallen zur ortsunabhängigen Präsentation von Fertigungsprozessen für Kunden und Bewerber |
| **Relevanz für VA** | Meeting Type (Vertriebspräsentation / Employer Branding), VR-Eignung (Fertigungsprozesse sehr hoch) |

**Was wurde gemacht?** Für traditionelle Industriebetriebe sind physische Werksführungen ein Kernstück des B2B-Vertriebs und des Employer Brandings. Enra dokumentiert, wie virtuelle Führungen diese Funktion übernehmen und gleichzeitig räumliche und zeitliche Beschränkungen aufheben. Kombinierte Formate (Rundgang + eingebettete Mitarbeiter-Videos) adressieren ein deutlich breiteres Publikum als reine Videoformate.

**Mehrwerte für KMU:** Jederzeit abrufbar (auch für internationale Kunden); erhöht Reichweite erheblich; kein Reiseaufwand für Interessenten.

**Herausforderungen:** Qualität der 3D-Erfassung der Fabrik (Laserscanning, Photogrammetrie) bestimmt die Überzeugungskraft der virtuellen Tour.

---

**ELEMENTS — VR-gestützte 3D-Badplanung für Handwerksbetriebe (Norddeutschland)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Kommerzielle Branchenlösung für Handwerk |
| **Organisation** | ELEMENTS (Zusammenschluss deutscher Sanitär-Fachhandwerker) |
| **Branche** | Sanitärhandwerk / Badausstellung |
| **Region** | Norddeutschland (Ausstellungen in Kiel, Hamburg, Bremen, Lübeck u. a.) |
| **Link / Quelle** | [ELEMENTS – Virtuelle Badplanung](https://www.elements-show.de/badplanung) |
| **Rolle von VR** | Endkunden begehen ihr geplantes Bad in VR, bevor der erste Stein gesetzt ist; emotionale Kaufentscheidung durch immersives Erleben |
| **Relevanz für VA** | Meeting Type (Kundenberatung / Verkaufsgespräch), VR-Eignung (Raumplanung / Konfiguration sehr hoch), Anwendungsfall (Handwerk / Einzelhandel) |

**Was wurde gemacht?** ELEMENTS setzt VR-Badvisualisierung in seinen norddeutschen Ausstellungen ein. Kunden begehen ihre individuelle Badplanung immersiv, erleben Materialien, Raumverhältnisse und Lichtszenarien — bevor Kaufentscheidung und Montageplanung abgeschlossen sind.

**Mehrwerte für KMU:**
- Direkte Norddeutschland-Präsenz (SH, Hamburg, Bremen)
- Sinkende Abbruchquote nach dem Beratungsgespräch durch emotionale Bindung
- Weniger Planungsänderungen nach Beauftragung
- Übertragbar auf: Fliesenleger, Küchenstudio-Handwerk, Innenausbau-KMU

**Herausforderungen:** Laufende Pflege der Produktdatenbanken (Armaturen, Fliesen, Sanitärobjekte) aufwändig und kostenintensiv.

---

**IKEA — Virtuelle Raumplanung und Produktvisualisierung (Schweden / Global)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Endkunden-Anwendung (B2C; Modell für KMU-Einzelhandel) |
| **Organisation** | IKEA |
| **Branche** | Einzelhandel / Möbeldesign |
| **Region** | Schweden (Globaler Rollout, inkl. Deutschland) |
| **Link / Quelle** | [IKEA AR/VR Marketing Case Study](https://esquanmarketing.com/ikea-a-case-study-on-the-impact-of-ar-and-vr-on-marketing/) |
| **Rolle von VR** | Kunden designen ihre Wunschküche oder ihr Wohnzimmer in VR in Originalgröße — Kaufentscheidung durch immersives Erleben unterstützt |
| **Relevanz für VA** | Anwendungsfall (Produktkonfiguration / Kaufentscheidungsunterstützung), VR-Eignung (Raumplanung und Produktauswahl sehr hoch) |

**Was wurde gemacht?** IKEA setzt neben AR (IKEA Place App) auch VR-Anwendungen wie den „IKEA VR Kitchen Visualizer" ein: Kunden können komplexe Küchen in Originalgröße in VR erleben, bevor sie bestellt sind. VR-Erlebnisse fördern Kaufabschlüsse und senken Retourenquoten nachweislich.

**Mehrwerte für KMU:** Referenzmodell für norddeutsche Möbel-KMU, Küchenstudios und Raumausstatter: das Prinzip ist auf jede Branche mit räumlichen Produkten übertragbar.

**Herausforderungen:** IKEA setzt eigenes IT-Team ein; für KMU gibt es SaaS-Alternativen (z. B. Roomle, Dreiview, Canoa).

---

## Kategorie 6: Virtuelle Meetings & digitale Arbeitswelten

*VR-Meetingplattformen, Enterprise-Collaboration, CI-konforme virtuelle Räume*

---

**Arthur Technologies — Enterprise-VR-Office für strategische Meetings (Düsseldorf / Global)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Kommerzielle VR-Office-Plattform |
| **Organisation** | Arthur Technologies |
| **Branche** | IT / Enterprise Software |
| **Region** | Düsseldorf, Deutschland (global eingesetzt) |
| **Link / Quelle** | [Arthur Technologies](https://arthur.digital/) |
| **Rolle von VR** | Permanente virtuelle Büroräume für bis zu 80 Personen gleichzeitig als fotorealistische Avatare; integriert Whiteboards, Jira, 3D-Visualisierungstools |
| **Relevanz für VA** | Meeting Type (strategisches Team-Meeting / Workshop), VR-Eignung (Remote-Teams sehr hoch), Marktprodukt verfügbar |

**Was wurde gemacht?** Arthur bietet Unternehmen wie PwC und Societe Generale vollständige virtuelle Arbeitswelten an. Besonderheit: fotorealistische Avatare (nicht Cartoon-Style), persistente virtuelle Büroräume und tief integrierte Collaboration-Tools (Jira, Dokumente, 3D-Objekte). Das System ist darauf ausgelegt, wiederkehrende strategische Meetings zu ersetzen — nicht nur gelegentliche Calls.

**Mehrwerte für KMU:**
- Deutsches Unternehmen (Düsseldorf) — DSGVO-Konformität einfacher realisierbar als bei US-Anbietern
- Fotorealistische Avatare erhöhen soziale Präsenz gegenüber Cartoon-Avataren (Meta Horizon Workrooms)
- Persistente Räume: Whiteboards und Dokumente bleiben sitzungsübergreifend erhalten

**Herausforderungen:**
- Enterprise-Pricing; für sehr kleine KMU ggf. unverhältnismäßig
- Fotorealistische Avatarqualität erfordert gute Kamera und Beleuchtung am Teilnehmer-Standort

---

**DEKOM — CI-konforme VR-Meetingräume (Hamburg)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Kommerzielle Systemhaus-Lösung für Konferenz- und Collaboration-Technik |
| **Organisation** | DEKOM AG |
| **Branche** | IT / Konferenztechnik |
| **Region** | Hamburg |
| **Link / Quelle** | [DEKOM – VR Collaboration](https://www.dekom.com/de-de/vr-collaboration/) |
| **Rolle von VR** | CI-konforme virtuelle Meetingräume im Unternehmens-Design; professioneller Außenauftritt bei virtuellen Kundenbesuchen und Team-Meetings |
| **Relevanz für VA** | Meeting Type (Kunden-Meeting / internes Team-Meeting), Markenidentität in VR, KMU-geeignetes Systemhaus-Modell |

**Was wurde gemacht?** DEKOM ermöglicht Unternehmen, VR-Meetingräume im eigenen Corporate Design zu konfigurieren — Logo, Farben, Firmeninterieur. Für Kundenmeetings entsteht ein professioneller Auftritt; für interne Meetings stärkt die vertraute Unternehmensumgebung die Identifikation. Als Hamburger Systemhaus bietet DEKOM KMU einen lokalen Ansprechpartner für Einrichtung und Support.

**Mehrwerte für KMU:**
- Hamburger Anbieter — lokaler Support und regionale Referenzen
- CI-Konformität: professioneller als generische Plattformen (Meta Workrooms)
- Systemhaus-Modell: Hardware, Software und Schulung aus einer Hand

**Herausforderungen:** Anpassungsaufwand für individuelle CI; laufende Wartungsverträge einkalkulieren.

---

**MeetinVR — Business-Kollaborations-Suite für Brainstorming und Präsentationen (Dänemark)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Kommerzielles SaaS-Produkt |
| **Organisation** | MeetinVR ApS |
| **Branche** | IT / Enterprise Collaboration |
| **Region** | Dänemark (relevante Nähe zum deutsch-dänischen Grenzraum) |
| **Link / Quelle** | [MeetinVR](https://www.meetinvr.com/) |
| **Rolle von VR** | Spezialisierte Räume für verschiedene Meeting-Typen (Huddle-Space bis Keynote-Venue); 3D-Modell-Import, Notizen „aufhängen", interaktive Whiteboards, räumliches Audio |
| **Relevanz für VA** | Meeting Type (Brainstorming / Verkaufspräsentation / Workshop), VR-spezifische Differenzierungsmerkmale (räumliches Audio, intuitive Interaktionen) |

**Was wurde gemacht?** MeetinVR bietet verschiedene spezialisierte VR-Meetingräume an — von kleinen Huddle-Spaces bis hin zu Keynote-Venues für größere Gruppen. 3D-Modelle können importiert und im Meeting interaktiv präsentiert werden. Das räumliche Audio (Klang aus Richtung der sprechenden Person) und natürliche Interaktionen (virtuelle Handschläge, Objektübergaben) differenzieren gegenüber Video-Calls.

**Mehrwerte für KMU:** Dänisches Unternehmen mit EU-Datenschutzrahmen; nähe zum norddeutschen Markt; günstigerer Einstieg als Arthur für kleinere Teams.

**Herausforderungen:** Marktpositionen der VR-Kollaborationsplattformen sind noch im Flux (Konsolidierungsphase); langfristige Plattformverfügbarkeit prüfen.

---

## Kategorie 7: Digitale Zwillinge & Prozessmonitoring

*Live-Monitoring, Prozessüberwachung, Betriebsdaten in 3D*

---

**Mittelstand-Digital Zentrum Schleswig-Holstein — Digitaler Zwilling für KMU**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Transferprojekt / Demonstratorangebot für KMU |
| **Organisation** | Mittelstand-Digital Zentrum Schleswig-Holstein |
| **Branche** | Branchenübergreifend (Produktion & Dienstleistung) |
| **Region** | Schleswig-Holstein (Labtouren z. B. in Lübeck) |
| **Link / Quelle** | [Digitaler Zwilling für KMU – MDZ SH](https://www.digitalzentrum-sh.de/themen/digitaler-zwilling) |
| **Rolle von VR** | Visuelle 3D-Darstellung live ablaufender Maschinenprozesse und Betriebszustände; immersiver Eindruck realer Abläufe über digitalen Zwilling |
| **Relevanz für VA** | Anwendungsfall (Prozessüberwachung / Zustandsüberwachung), VR-Eignung (Betriebsdaten-Visualisierung mittel bis hoch) |

**Was wurde gemacht?** Das MDZ Schleswig-Holstein unterstützt SH-KMU beim Aufbau digitaler Zwillinge für ihre Produktionsanlagen. Physische Maschinen werden über 3D-Modelle live überwacht und gesteuert. Kleinste Prozessauffälligkeiten werden frühzeitig sichtbar — Wartung kann proaktiv geplant werden statt reaktiv bei Ausfall.

**Mehrwerte für KMU:**
- Direkte SH-Relevanz: regionale Beratung und Demonstratoren kostenfrei nutzbar
- Frühwarnsystem: Maschinenstillstände vermeiden, Wartungsintervalle optimieren
- Einstieg auch mit einfachen IoT-Sensoren und 2D-Dashboards möglich — VR/3D als nächste Eskalationsstufe

**Herausforderungen:** Qualität des digitalen Zwillings hängt von Sensor-Coverage und Datenpflege ab; einmalige Einrichtung ist aufwändig.

---

**EWE AG — Virtuelle Bürgerbeteiligung bei Netzausbau (Oldenburg, Niedersachsen)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Unternehmensimplementierung / Kommunikationsprojekt |
| **Organisation** | EWE AG |
| **Branche** | Energieversorgung / Netzinfrastruktur |
| **Region** | Oldenburg, Niedersachsen |
| **Link / Quelle** | [EWE – Digitale Zwillinge in der Energieversorgung](https://www.ewe.de/ueber-ewe/digitalisierung) |
| **Rolle von VR** | Geplante Umspannwerke und Trassenverläufe werden in VR visualisiert; Bürger können die Auswirkungen auf das Landschaftsbild realitätsnah einschätzen |
| **Relevanz für VA** | Anwendungsfall (Stakeholder-Kommunikation / Bürgerdialog), VR-Eignung (räumliche Planung und öffentliche Akzeptanz) |

**Was wurde gemacht?** EWE nutzt VR, um geplante Netzinfrastrukturprojekte (Umspannwerke, Freileitungen, Kabeltrassen) für Bürger und Behörden visuell erfahrbar zu machen. Die Akzeptanz von Infrastrukturprojekten steigt, wenn Betroffene die visuelle Auswirkung auf ihre Umgebung realistisch einschätzen können, bevor gebaut wird.

**Mehrwerte für KMU:** Übertragbar auf KMU im Bereich kommunaler Infrastruktur, Tiefbau, Windparkplanung und Stadtentwicklung in Norddeutschland.

**Herausforderungen:** Erstellung präziser Geodatenmodelle der Umgebung aufwändig (Drohnenbefliegung, GIS-Integration).

---

## Kategorie 8: Branchenspezifisch — Pflege & Gesundheit

*Therapie, klinische Planung, medizintechnische Anwendungen*

---

**Mittelstand-Digital Zentrum Rostock — VR in der Pflege**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Umsetzungsprojekt / Demonstrator |
| **Organisation** | Mittelstand-Digital Zentrum Rostock in Kooperation mit einem regionalen Pflegebetrieb |
| **Branche** | Gesundheitswesen / Pflege / Soziale Dienstleistungen |
| **Region** | Rostock, Mecklenburg-Vorpommern |
| **Link / Quelle** | [Digitalzentrum Rostock – VR in der Pflege](https://www.digitalzentrum-rostock.de/praxisbeispiele/umsetzungsprojekte/virtual-reality-in-pflege/) |
| **Rolle von VR** | Schaffung therapeutischer Mehrwerte für Pflegeheimbewohner durch immersive Erlebniswelten (z. B. virtuelle Reisen, Naturerlebnisse) |
| **Relevanz für VA** | Anwendungsfall (therapeutische VR / Wohlbefinden), VR-Eignung (zugangsbeschränkte Erlebnisse sehr hoch), KMU-relevante Branche (kleine Pflegebetriebe) |

**Was wurde gemacht?** Das MDZ Rostock entwickelte gemeinsam mit einem Pflegebetrieb ein Konzept für VR als Therapieergänzung. VR-Brillen ermöglichen Bewohnern immersive Erlebnisse (Strandspaziergänge, Bergwanderungen, historische Orte), die ihnen physisch nicht mehr zugänglich sind. Ein besonderer Fokus lag auf der Benutzerfreundlichkeit für ältere Nutzer und das Pflegepersonal (einfache Bedienung, Hygienekonzept).

**Mehrwerte für KMU:**
- Direkter therapeutischer Mehrwert: Lebensqualität der Bewohner messbar gesteigert
- Differenzierungsmerkmal für kleine Pflegebetriebe im Wettbewerb um Bewohner und Fachkräfte
- Kostenlose Erprobung via MDZ-Demonstrator als Einstieg

**Herausforderungen:**
- DSGVO und Datenschutz bei biometrischen Daten (Augenverfolgung) in Pflegekontext besonders sensibel
- Hygienekonzept für Headset-Sharing zwingend erforderlich (→ auch relevant für Kap. 08)
- Akzeptanz bei sehr alten oder kognitiv eingeschränkten Bewohnern individuell verschieden

---

**Olympus Winter & Ibe GmbH — Virtuelle OP-Planung und Produktkonfiguration (Hamburg)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | Unternehmensimplementierung (weltweiter B2B-Vertrieb) |
| **Organisation** | Olympus Winter & Ibe GmbH |
| **Branche** | Medizintechnik |
| **Region** | Hamburg |
| **Link / Quelle** | [Olympus – Digital Solutions](https://www.olympus-europa.com/medical/de/Products-and-Solutions/Solutions/Digital-Solutions.html) |
| **Rolle von VR** | Chirurgen und Klinikplaner konfigurieren die Anordnung von Endoskopietürmen und chirurgischen Geräten im OP virtuell — Ergonomie und Raumplanung optimieren |
| **Relevanz für VA** | Anwendungsfall (Produktkonfiguration / OP-Planung), Meeting Type (B2B-Vertrieb / Co-Design), VR-Eignung (komplexe räumliche Konfiguration sehr hoch) |

**Was wurde gemacht?** Olympus Winter & Ibe nutzt VR, um Kliniken und Chirurgen die Konfiguration und Positionierung von Endoskopiegeräten im OP-Umfeld zu ermöglichen, bevor Kaufentscheidung und Inbetriebnahme erfolgen. Ergonomie, Zugänglichkeit und Geräteplatzierung werden in VR validiert.

**Mehrwerte für KMU:** Hamburger Medizintechnik-KMU als Zielgruppe: VR ersetzt aufwändige physische Showrooms und Demo-Räume für erklärungsbedürftige Produkte.

**Herausforderungen:** Regulatorische Anforderungen im medizinischen Umfeld (CE-Kennzeichnung, MDR) sind komplex; DSGVO-Sensibilität bei Klinikundaten.

---

## Kategorie 9: Bauwesen & Architektur

---

**Mittelstand-Digital Zentrum Bau & Zukunftskultur — XR für das „Kreativ Quartier" Potsdam (Hannover Messe)**

| Eigenschaft | Wert |
|---|---|
| **Typ** | XR-Demonstrator / Messe-Case |
| **Organisation** | MDZ Bau, MDZ Zukunftskultur, Architekturbüro &Mica, XR-Designerin Anke Schiemann |
| **Branche** | Bauwesen / Architektur / nachhaltige Stadtentwicklung |
| **Region** | Hannover Messe (Niedersachsen) / Potsdam |
| **Link / Quelle** | [Digitalzentrum Bau – Kreative und immersive Arbeitswelten](https://www.digitalzentrumbau.de/kos/WNetz?art=Appointment.show&id=1050) |
| **Rolle von VR/XR** | Immersives Erfahrbar-Machen von Nachhaltigkeitsaspekten (Zirkularität, Emissionen, Materialherkunft) im Entstehungsprozess eines Stadtquartiers |
| **Relevanz für VA** | Anwendungsfall (Stakeholder-Kommunikation / nachhaltige Planung), VR-Eignung (abstrakte Konzepte visuell vermitteln sehr hoch) |

**Was wurde gemacht?** Anhand des realen Bauprojekts „Kreativ Quartier Potsdam" wurde ein XR-Demonstrator entwickelt, der abstrakte Nachhaltigkeitsinformationen (CO₂-Emissionen, Materialherkunft, Kreislaufwirtschaft) für Bauträger, Handwerker und Architekten vor Ort erlebbar macht — via Tablet und XR-Brille, direkt auf der Baustelle.

**Mehrwerte für KMU:** Zeigt, dass VR/AR nicht nur für Produktion relevant ist: Architektur- und Bau-KMU in Norddeutschland können Nachhaltigkeitskonzepte gegenüber Investoren und Behörden immersiv kommunizieren — ein Differenzierungsmerkmal.

**Herausforderungen:** Inhaltliche Tiefe der XR-Darstellung (akkurate Materialien-Daten, Emissionswerte) erfordert gute Datenbasis; Pflege bei Planungsänderungen.

---

## Übersichtstabelle aller Einträge

| # | Organisation | Kategorie | Region | Typ | Norddeutschland-Bezug |
|---|---|---|---|---|---|
| 1 | HellermannTyton & HAW Hamburg | Training | Tornesch, SH / HH | KMU-Kooperation | **Direkt (SH)** |
| 2 | Fraunhofer IML | Training | Dortmund / Hamburg/Bremen | Angewandte Forschung | Indirekt (Branche) |
| 3 | TeamViewer Frontline | Training / Fernwartung | Bremen / Global | SaaS | **Ja (Bremen)** |
| 4 | Vestas / VRAI | Training / Marketing | Dänemark | Kooperation | Ja (Offshore-Relevanz SH/NDS) |
| 5 | MDZ Hamburg – Onboarding | Training | Hamburg | Demonstrator | **Direkt (HH)** |
| 6 | MDZ SH – Montageplanung | Fabrikplanung | Schleswig-Holstein | Demonstrator | **Direkt (SH)** |
| 7 | Halocline GmbH | Fabrikplanung | Osnabrück, NDS | SaaS | Ja (NDS) |
| 8 | Digital Reality Academy | Fabrikplanung | Hannover, NDS | Transfer-Hub | Ja (NDS) |
| 9 | Hochschule Koblenz | Fabrikplanung | RLP (übertragbar) | Case Study | Methodik |
| 10 | Krones AG | Fabrikplanung | Bayern / Kunden NDS | Engineering-Tool | Indirekt |
| 11 | Drägerwerk AG | Prototyping | Lübeck, **SH** | Unternehmensimpl. | **Direkt (SH)** |
| 12 | Team Malizia / VRtual X | Prototyping | **Hamburg** | Kooperation | **Direkt (HH)** |
| 13 | Lufthansa Technik | Prototyping / Vertrieb | **Hamburg** | Unternehmensimpl. | **Direkt (HH)** |
| 14 | Airbus | Prototyping | **Hamburg** | Unternehmensimpl. | **Direkt (HH)** |
| 15 | Hololight | Prototyping | München (DE) | SaaS | Deutschlandweit |
| 16 | Volvo Cars | Prototyping | Schweden | Case Study | Referenz |
| 17 | KONE / Tampere Univ. | Prototyping | Finnland | Peer-reviewed | Referenz |
| 18 | MDZ Bremen/Hamburg – Maritime Wartung | Fernwartung | Bremen / **HH** | Demonstrator | **Direkt (HH/HB)** |
| 19 | Fette Compacting | Fernwartung | Schwarzenbek, **SH** | Unternehmensimpl. | **Direkt (SH)** |
| 20 | SMS Group | Fernwartung | Düsseldorf / Intl. | Praxiseinsatz | Referenz |
| 21 | Jungheinrich AG | Vertrieb / Showroom | **Hamburg** | Vertriebstool | **Direkt (HH)** |
| 22 | enra GmbH | Vertrieb / Werksführung | DE-weit | Leitfaden | Übertragbar |
| 23 | ELEMENTS | Vertrieb / Handwerk | Norddeutschland | Branchenlösung | **Direkt (Nord)** |
| 24 | IKEA | Vertrieb / Showroom | Global | B2C-Referenz | Referenz |
| 25 | Arthur Technologies | Meetings | Düsseldorf / Global | SaaS | Ja (DE) |
| 26 | DEKOM AG | Meetings | **Hamburg** | Systemhaus | **Direkt (HH)** |
| 27 | MeetinVR | Meetings | Dänemark | SaaS | Ja (Grenzraum) |
| 28 | MDZ SH – Digitaler Zwilling | Digitaler Zwilling | Schleswig-Holstein | Demonstrator | **Direkt (SH)** |
| 29 | EWE AG | Digitaler Zwilling | Oldenburg, NDS | Unternehmensimpl. | Ja (NDS) |
| 30 | MDZ Rostock – Pflege | Pflege & Gesundheit | Rostock, MV | Demonstrator | Ja (Norddeutsch) |
| 31 | Olympus Winter & Ibe | Pflege & Gesundheit | **Hamburg** | Unternehmensimpl. | **Direkt (HH)** |
| 32 | MDZ Bau – Kreativ Quartier | Bauwesen | Hannover / Potsdam | Demonstrator | Ja (NDS) |
| — | ~~Meyer Werft~~ | ~~Prototyping~~ | ~~Papenburg~~ | **bereits in Kap. 04** | — |
