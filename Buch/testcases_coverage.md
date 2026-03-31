---
title: "Testfälle: Buchdeckungsanalyse"
status: "Arbeitsdokument (nicht für Publikation)"
---

> **Zweck dieses Dokuments**: 20 typische Organisationen aus Schleswig-Holstein, die VR ernsthaft in Betracht ziehen könnten. Für jeden Fall werden konkrete Fragen, Rahmenbedingungen und Datenschutzrelevanz dokumentiert. Anschließend wird bewertet, ob das Handbuch diese Fragen derzeit beantwortet. Das Dokument dient als iterative Prüfinstanz: Lücken werden identifiziert, priorisiert und sukzessive geschlossen — durch Buchkapitel, eigene Experimente oder externe Referenzen.
>
> **Status-Legende**: ✅ Buch beantwortet dies hinreichend · ⚠️ Teilantwort vorhanden, Vertiefung nötig · ❌ Nicht abgedeckt

---

## Legende der Felder

| Feld | Beschreibung |
|---|---|
| **Profil** | Branche, Größe, Standort SH |
| **VR-Frage** | Was die Organisation konkret wissen will |
| **Kernbedürfnis** | Welchen Nutzen sie sich von VR verspricht |
| **Besonderheiten** | Constraints (Datenschutz, Budget, Belegschaft, Regulierung) |
| **Buchdeckung** | Was das Handbuch derzeit beantwortet — und was fehlt |

---

## Fall 01 — Tischlerei mit Küchen- und Möbelauftragsfertigung

**Profil**: Handwerksbetrieb, 9 Mitarbeitende, Schleswig. Fertigt Einbauküchen und Möbel nach Maß. Wächst durch Empfehlungsmarketing. Keine eigene IT-Abteilung.

**VR-Frage**: „Können unsere Kunden die Küche vor dem Kauf in VR begehen — und verringert das spätere Reklamationen?"

**Kernbedürfnis**: Kundenkommunikation verbessern, teure Nachänderungen vermeiden, sich von Möbeldiscountern differenzieren.

**Besonderheiten**:
- Budget ca. 3.000–8.000 € einmalig, keine laufenden IT-Kosten
- Keine VR-Vorerfahrung im Team; Inhaber ist 54 Jahre alt
- Kundendaten (Name, Adresse, Aufmaß) dürfen nicht in US-Cloud-Dienste
- DSGVO: Meta Quest für Kundenpräsentationen ungeeignet (Nutzerdaten an Meta) → Alternativsystem nötig
- Lösungsreife: Marktprodukte existieren (z. B. RoomSketcher VR, IKEA Place, Einzellösungen auf Meta Quest ohne Konto-Zwang prüfbar)

**Buchdeckung**:
- ✅ Kap. 03: Kosten-Nutzen-Rahmen, Customer Experience als BN-Knoten
- ✅ Kap. 04: Anwendungsfall Produktkonfiguration / Kundenpräsentation ist als VA-Typ abgedeckt
- ⚠️ Kap. 07: ATI und Onboarding für Inhaber 54+ thematisiert, aber kein spezifisches Szenario „Kunde als Einmalprobant"
- ⚠️ Kap. 08: Datenschutz grundsätzlich erwähnt; Meta-spezifische DSGVO-Problematik bei Kundenpräsentationen **nicht explizit**
- ❌ ROI-Kalkulation für Kleinstbetriebe (<10 MA) mit einmaligem Setup-Investment fehlt
- ❌ Marktübersicht „schlüsselfertige Konfigurator-Lösungen" für Handwerk fehlt

---

## Fall 02 — Schiffsreparatur- und Wartungswerft

**Profil**: Werftbetrieb, 38 Mitarbeitende, Kiel. Wartung und Reparatur von Segelyachten bis Motorbooten. Spezialkompetenz: Rigg und Segel. Arbeiten am und über Wasser, in engen Schiffsräumen.

**VR-Frage**: „Können wir neue Monteure sicherer in Arbeiten unter Deck oder in der Takelage einweisen, bevor sie echte Fehler machen?"

**Kernbedürfnis**: Arbeitssicherheitsschulung in gefährlichen Umgebungen ohne reales Unfallrisiko; Einarbeitung neuer Mitarbeitender aus EU-Ausland (Sprachbarriere).

**Besonderheiten**:
- Fachkräftemangel: Rekrutierung aus Polen, Portugal; Sprachvielfalt
- Arbeit in beengten Räumen → physiologisch herausforderndes VR-Setting (Klaustrophobie-Risiko)
- Trainingsinhalte sind proprietäres Know-how: Datenspeicherung muss lokal möglich sein
- Keine Cloud-Abhängigkeit akzeptabel für interne Verfahrensdokumentation
- Schutzkleidung (Handschuhe) macht Controller-Bedienung schwierig → Handtracking prüfen

**Buchdeckung**:
- ✅ Kap. 04: VR-Training für prozedurale Skills wissenschaftlich belegt (Sitzmann 2011)
- ✅ Kap. 07: Motion Sickness in engen VR-Räumen, ATI als Moderator
- ⚠️ Kap. 08: Lokale vs. Cloud-Deployment kurz erwähnt, aber kein konkreter Leitfaden für „keine Cloud"
- ❌ Mehrsprachige Lernumgebungen in VR: nicht abgedeckt
- ❌ Handtracking als Alternative zu Controllern bei Schutzausrüstung: nicht thematisiert
- ❌ Klaustrophobie-Risiko bei beengten VR-Szenarien: nicht abgedeckt

---

## Fall 03 — Sportbootgutachterbüro

**Profil**: Einzelunternehmen, 1 Mitarbeitender + gelegentliche Subunternehmer, Schleswig-Holstein Küstenregion. Erstellt Wert- und Schadensgutachten für Sportboote (Kauf, Versicherung, Streitfälle).

**VR-Frage**: „Kann ich einem Kunden oder Auftraggeber in Hamburg ein Gutachten präsentieren, ohne dass er oder ich reisen muss — und mit ausreichend visuellen Details, damit das Gutachten nachvollziehbar ist?"

**Kernbedürfnis**: Zeit- und Reisekostenersparnis; Gutachten für Auftraggeber nachvollziehbarer machen; Fernkollaboration mit Reedereien oder Versicherungen.

**Besonderheiten**:
- **Eigenes Experiment bereits durchgeführt** (→ Kap. 06 / Anhang): 360°-Fotografie in VR als Grundlage für Bootsgutachten mit Stefan Bruns (sportboot-gutachter.de)
- **LIDAR-Scanning-Experiment** ebenfalls durchgeführt (iPhone 15 Pro): Ergebnis — zu unreif für professionelle Detailarbeit
- Gutachtendaten unterliegen ggf. Verschwiegenheitspflichten / Auftragsrecht
- Kein IT-Budget; Lösung muss auf Consumer-Hardware basieren
- Auftraggeber (Versicherungen) könnten eigene IT-Compliance-Anforderungen haben

**Buchdeckung**:
- ✅ Kap. 04: Remote-Inspection als Meeting-Typ thematisiert
- ⚠️ Kap. 06: Eigene Studie erwähnt VR für Verhandlungen, aber 360°-Gutachten-Use-Case **noch nicht eingearbeitet**
- ❌ 360°-Fotografie als VR-Inhalt: Technik und Grenzen nicht beschrieben
- ❌ LIDAR-Scanning: Experiment und Ergebnis (zu unreif) **noch nicht dokumentiert** → OFFENE_PUNKTE H1
- ❌ Use Case „Einzelgutachter": ROI-Rechnung für 1-Personen-Betrieb fehlt
- ❌ Qualitätsanforderungen professioneller Gutachten in VR: nicht thematisiert

---

## Fall 04 — Maschinenbauer (Sondermaschinenbau)

**Profil**: Mittelständischer Hersteller, 85 Mitarbeitende, Neumünster. Entwickelt und baut kundenspezifische Produktionsanlagen. Langer Verkaufszyklus (6–18 Monate), internationale Kunden.

**VR-Frage**: „Können wir einer Einkaufskommission in Japan unsere noch nicht fertiggestellte Anlage so realistisch präsentieren, dass sie kauft — ohne einen physischen Prototypen bauen zu müssen?"

**Kernbedürfnis**: Prototyping-Kosten reduzieren; internationale Kundenbindung ohne Reisen; Vertriebszyklus verkürzen.

**Besonderheiten**:
- CAD-Daten vorhanden (SolidWorks), aber VR-Konvertierung technisch anspruchsvoll
- Wettbewerbssensible Konstruktionsdaten dürfen nicht auf fremde Server
- Japanische Kunden: kulturelle VR-Akzeptanz möglicherweise höher als im deutschen Mittelstand
- IT-Abteilung vorhanden (2 Personen), aber kein VR-Know-how
- Mögliche Synergien mit Kap. 09-Trend: Digital Twin + VR

**Buchdeckung**:
- ✅ Kap. 03: Ford-Beispiel (berg2017) direkt vergleichbar (VR-Prototyping im Maschinenbau)
- ✅ Kap. 05: ROI-Zahlen aus Berg et al. 2017 zitiert
- ⚠️ Kap. 08: CAD-zu-VR-Konvertierungspipeline nicht konkret beschrieben
- ❌ Datenschutz bei CAD-Daten in VR: Betriebsgeheimnisschutz nicht thematisiert
- ❌ Kulturelle Unterschiede bei VR-Präsentationen (Japan vs. DE): Kap. 07 erwähnt Kultur nur für DK-DE
- ❌ Konkrete Software-Lösungen für CAD→VR (z. B. Scope AR, IrisVR, Autodesk Forma): nicht gelistet

---

## Fall 05 — Landwirtschaftsbetrieb mit Lohnunternehmen

**Profil**: Familienbetrieb, 12 Festangestellte + 8 Saisonkräfte, Angeln (Kreis SL-FL). Ackerbau, Rinderhaltung, Lohnunternehmen für Nachbarbetriebe. Jedes Jahr neu rekrutierte Saisonkräfte aus Rumänien und der Ukraine.

**VR-Frage**: „Können wir unsere Saisonarbeiter in Maschinenbedienung und Sicherheitsvorschriften einweisen, ohne dass der Betriebsleiter jedes Mal drei Tage verliert?"

**Kernbedürfnis**: Einarbeitungszeit reduzieren; Unfallrisiko senken; Sprachbarriere überbrücken.

**Besonderheiten**:
- Saisonkräfte haben keine Smartphone-/IT-Erfahrung mit Komplexsystemen
- Extrem niedrige ATI-Werte wahrscheinlich
- WLAN-Infrastruktur auf Feldern/in Ställen nicht vorhanden → Offline-VR zwingend
- Mehrsprachigkeit: Rumänisch, Ukrainisch, teilweise kein Deutsch
- Budget sehr begrenzt; EU-Fördermittel (ELER) für Digitalisierung möglicherweise nutzbar

**Buchdeckung**:
- ✅ Kap. 07: Niedrige ATI-Werte und entsprechende Onboarding-Empfehlungen
- ✅ Kap. 04: Schulungsszenarien für prozedurale Skills belegt
- ⚠️ Kap. 08: Offline-Deployment theoretisch möglich (Standalone), aber nicht explizit behandelt
- ❌ Mehrsprachige VR-Inhalte: komplett fehlend
- ❌ Landwirtschaft / Agraranwendungen: kein Beispiel, keine Branchenspezifik
- ❌ Fördermöglichkeiten (EU, SH-spezifisch): nicht abgedeckt
- ❌ VR mit sehr niedrigen ATI-Basiswerten und Analphabetismus-Risiko: nicht thematisiert

---

## Fall 06 — Pflegeeinrichtung (stationäre Altenpflege)

**Profil**: Gemeinnützige gGmbH, 60 Mitarbeitende, Schleswig. Stationäre Pflege, Kurzzeitpflege, Tagespflege. Kirchlicher Träger.

**VR-Fragen**: (a) „Können wir VR für Demenzbewohner als kognitive Stimulation einsetzen?" (b) „Können wir Pflege-Azubis in schwierigen Situationen (Aggressivität, Sturz) trainieren?"

**Kernbedürfnis**: Lebensqualität der Bewohner verbessern; Azubi-Ausbildung realitätsnäher machen; Fachkräftebindung durch innovative Ausbildung.

**Besonderheiten**:
- **Datenschutz höchste Priorität**: Patientendaten, Bewohnerdaten — keinerlei Weitergabe an US-Dienste
- Meta Quest vollständig inakzeptabel für Bewohnerkontakt (Biometrie, Werbeprofiling)
- Kirchlicher Träger: ethische Grundsätze für Technologieeinsatz mit vulnerablen Personen
- Personal hat kaum Zeit für Schulungen; Azubis haben heterogene Vorerfahrungen
- Demenztherapie-Anwendungen: klinisch validierte Produkte erforderlich

**Buchdeckung**:
- ⚠️ Kap. 07: VR-Sickness und vulnerable Gruppen kurz erwähnt, Demenzpatienten nicht spezifisch
- ⚠️ Kap. 08: Datenschutz allgemein erwähnt; Meta-DSGVO-Problem **nicht explizit**
- ❌ Gesundheitssektor / klinisch validierte VR-Anwendungen: nicht abgedeckt
- ❌ VR mit vulnerablen Personengruppen (Demenz, Pflegebedürftigkeit): komplett fehlend
- ❌ Kirchlich-ethische Rahmenbedingungen für Technologieeinsatz: nicht thematisiert
- ❌ Zertifizierungs- und Medizinprodukterecht (MDR) für therapeutische VR: nicht abgedeckt

---

## Fall 07 — Messebau-/Eventmarketing-Unternehmen

**Profil**: Kreativagentur, 22 Mitarbeitende, Flensburg-Umgebung. Plant und baut Messestände für regionale KMU. Kooperationspartner: Omnicon Group, Neox Studios.

**VR-Frage**: „Können wir unseren KMU-Kunden einen virtuellen Messestand anbieten, damit sie auf Messen präsent sind, ohne den physischen Aufwand?"

**Kernbedürfnis**: Neues Dienstleistungsangebot; Differenzierung vom Wettbewerb; Kunden die Kosten großer physischer Messepräsenzen ersparen.

**Besonderheiten**:
- **Eigenes Experiment bereits durchgeführt**: VR-Messestand-Projekt in Zusammenarbeit mit Orion/Omnicon Group/Neox Studios Flensburg (→ dokumentieren)
- Neues Geschäftsmodell: Agentur als VR-Dienstleister, nicht nur Messestand-Bauer
- Kunden der Agentur: breites KMU-Spektrum — heterogene IT-Kompetenz
- Frage der Plattformwahl: eigene App vs. bestehende VR-Messe-Plattformen
- Datenschutz: Besucher-Tracking in virtuellen Messeständen (Verhaltensprofile) — ethisch/rechtlich prüfen

**Buchdeckung**:
- ✅ Kap. 03: Employer Branding und Customer Experience als BN-Knoten
- ✅ Kap. 04: Marketing/Präsentation als Meeting-Typ prinzipiell enthalten
- ⚠️ Kap. 09: VR-Messe als Trend erwähnt, aber kein konkretes Produktbeispiel
- ❌ **Eigenes VR-Messestand-Experiment: noch nicht eingearbeitet** → OFFENE_PUNKTE H3
- ❌ Agentur als VR-Dienstleister (Geschäftsmodell-Perspektive): nicht abgedeckt
- ❌ Besucher-Tracking-Ethik in VR-Ständen: nicht thematisiert

---

## Fall 08 — Steuerberatungskanzlei

**Profil**: Partnerschaftsgesellschaft, 14 Mitarbeitende (6 Berater, 8 Assistenz), Kiel. Mandanten hauptsächlich SH-KMU und Freiberufler.

**VR-Frage**: „Können wir Jahresabschlussgespräche mit Mandanten in VR führen, wenn diese nicht persönlich kommen können?"

**Kernbedürfnis**: Servicequalität bei Remote-Mandanten; Besprechungen effizienter als Videokonferenzen gestalten.

**Besonderheiten**:
- **Steuergeheimnis (§ 30 AO)** und **berufsrechtliche Verschwiegenheitspflicht**: absolute Datentrennung von Drittdiensten
- Meta Quest: vollständig inkompatibel. Alle Gesprächsdaten, Metadaten, ggf. Sprachaufzeichnungen wären auf US-Servern
- ULD Schleswig-Holstein würde Meta-Quest-Einsatz in mandantenbezogenen Gesprächen mit hoher Wahrscheinlichkeit beanstanden
- Mandanten: ältere Generation (Ø 52 Jahre), heterogene Technikaffinität
- Alternative Plattformen mit DSGVO-Konformität und On-Premise-Option nötig (z. B. Mozilla Hubs Self-Hosted, VirbEla Enterprise)

**Buchdeckung**:
- ✅ Kap. 05: UTAUT — Social Influence als Adoptionsfaktor relevant für Mandantenakzeptanz
- ✅ Kap. 07: Alter und ATI als Moderatoren
- ❌ **Berufsgeheimnisschutz und VR**: komplett fehlend — kritische Lücke
- ❌ **Meta Quest DSGVO-Inkompatibilität**: nicht explizit — kritische Lücke
- ❌ DSGVO-konforme VR-Alternativen zu Meta (selbst-gehostete Lösungen): nicht beschrieben
- ❌ ULD SH als Aufsichtsbehörde: nicht erwähnt

---

## Fall 09 — Architekturbüro

**Profil**: Bürogemeinschaft, 7 Mitarbeitende, Flensburg. Entwirft Wohngebäude und kleinere Gewerbebauten. Nutzt ArchiCAD, gelegentlich Revit.

**VR-Frage**: „Können wir Bauherren unsere Entwürfe in VR zeigen, bevor die Baugenehmigung beantragt wird — und bekommen wir so weniger Änderungswünsche nach Baubeginn?"

**Kernbedürfnis**: Kundenzufriedenheit; Planungssicherheit; Differenzierung gegenüber größeren Büros.

**Besonderheiten**:
- ArchiCAD → VR-Export: technisch möglich (z. B. via Enscape, Twinmotion, D5 Render)
- Bauherren-Daten gelten als Kundendaten; Meta-Konto für Bauherren beim Kanzleibesuch unzumutbar
- Walk-through-VR für Laien: sehr niedrige ATI, erste VR-Erfahrung oft beim Architektentermin
- Körperliches Setup: Bauherren sitzen mit Headset — Stuhlrotation, kurze Session nötig
- Lizenzkosten für Enscape/Twinmotion relevant; Weitergaberecht der VR-Szene an Bauherren prüfen

**Buchdeckung**:
- ✅ Kap. 04: Produktvisualisierung / Kundenpräsentation als VR-Anwendungsfall
- ✅ Kap. 07: Erstnutzer, Onboarding, kurze Sessions für Nicht-IT-Nutzer
- ⚠️ Kap. 03: IKEA-Place-Beispiel (Produktkonfiguration) angrenzend, aber nicht Architektur
- ❌ ArchiCAD/Revit → VR-Pipeline: nicht beschrieben
- ❌ Konkrete Softwareprodukte (Enscape, Twinmotion, D5 Render): nicht aufgeführt
- ❌ Bauherren als einmalige, technisch unerfahrene VR-Nutzer: Sonderfall nicht adressiert

---

## Fall 10 — Tourismusmarketing-Agentur (Küstentourismus)

**Profil**: GmbH, 11 Mitarbeitende, Husum. Vermarktet touristische Angebote entlang der Nordseeküste SH. Kunden: Hotels, Campingplätze, Freizeitanbieter.

**VR-Frage**: „Können wir potenziellen Urlaubern auf Reisemessen in Frankfurt oder online eine VR-Vorschau unserer Küstenregion geben?"

**Kernbedürfnis**: Emotionalisierung des Marketings; Vorabbegeisterung für Buchungen; Differenzierung im Messeauftritt.

**Besonderheiten**:
- Inhalte: 360°-Videos und -Fotos der Küste — Produktion intern möglich
- Messeauftritte: Headsets an wechselnden Standorten, robuste Hardware nötig
- Besucher-Tracking (wer hat was geschaut?) wäre für Marketing wertvoll — aber DSGVO-sensitiv
- Meta Quest für Messe-Demonstrationen: problematisch wenn Benutzerkonten erforderlich (Gast-Modus als Workaround möglich, aber Datenlage unklar)
- Niederländische und dänische Touristen: mehrsprachige Inhalte

**Buchdeckung**:
- ✅ Kap. 03: Customer Experience und Employer Branding als BN-Knoten
- ✅ Kap. 09: Immersive Customer Experience als wirtschaftlicher Trend (Flavián 2019)
- ⚠️ Kap. 04: Marketing-Anwendungsfall prinzipiell erwähnt, kein Tourismus-spezifisches Beispiel
- ❌ 360°-Video als VR-Inhalt: Produktion, Kosten, Qualitätsanforderungen nicht beschrieben
- ❌ Messe-Setup mit VR (Hygiene, Logistik, Gästemodus): nicht abgedeckt
- ❌ Tourismus SH als Branche: kein spezifisches Beispiel

---

## Fall 11 — Berufsschule / Berufliches Gymnasium (Handwerk + Technik)

**Profil**: Öffentliche Berufsschule, 180 Schüler/Azubis, Rendsburg. Ausbildungsberufe: Elektroniker, Mechatroniker, Anlagenmechaniker SHK.

**VR-Frage**: „Können wir Azubis gefahrenträchtige Arbeitsschritte (Hochspannung, Schweißen, Gasinstallation) in VR üben, bevor sie es an echten Anlagen tun?"

**Kernbedürfnis**: Unfallprävention; Ausbildungsqualität; Attraktivität der Schule für Betriebe.

**Besonderheiten**:
- Öffentlicher Träger: Beschaffung über Ausschreibung (VOB/VOL), lange Vorlaufzeiten
- Datenschutz Schüler: Besonderer Schutz Minderjähriger; Schulbehörde SH hat eigene IT-Vorgaben
- Leihgeräte für 30 Schüler gleichzeitig: Hygiene (Brillenträger), Headset-Sharing-Konzept
- Lehrplan-Integration: VR-Einheiten müssen in Stundenplan passen
- Bestehende Lernmanagementsysteme (Moodle) als Anforderung für Integration

**Buchdeckung**:
- ✅ Kap. 04: Sitzmann (2011) — Schulungswirksamkeit VR für prozedurale Skills
- ✅ Kap. 07: Altersgruppe Jugendliche: schnellere Adaption, niedrigere Effort Expectancy
- ⚠️ Kap. 03: Employer Branding / Talentpool für Betriebe erwähnt, Schulperspektive nicht
- ❌ Öffentliche Beschaffung und Ausschreibungspflicht: komplett fehlend
- ❌ Hygiene-Konzept für Headset-Sharing: nicht thematisiert
- ❌ Datenschutz Minderjähriger in VR: nicht abgedeckt
- ❌ Lehrplan- und LMS-Integration: nicht abgedeckt

---

## Fall 12 — Windenergie-Servicedienstleister

**Profil**: GmbH, 45 Mitarbeitende, Husum. Wartung und Inspektion von Windkraftanlagen (Onshore + erste Offshore-Projekte). Kunden: Windparkbetreiber in SH und Dänemark.

**VR-Frage**: „Können neue Techniker in VR auf einer simulierten Anlage trainieren, bevor sie das erste Mal 100 Meter hoch klettern?"

**Kernbedürfnis**: Arbeitssicherheit; Zertifizierungsnachweis; Rekrutierung internationaler Fachkräfte mit sprachübergreifendem Training.

**Besonderheiten**:
- Sehr hohe Sicherheitsrelevanz: Fehler können tödlich sein; Versicherungs- und Haftungsfragen
- Training muss nachweisbar dokumentiert sein (Zertifizierung, ISO-Normen)
- Anlageninformationen (Turm-Layouts, Steuerungssoftware) sind sensibel — kein Cloud-Upload
- Grenzüberschreitend DK-DE: dänische und deutsche Arbeitsschutzstandards kombinieren
- Offshore zunehmend relevant: Seekrankheit kann Motion-Sickness-Anfälligkeit erhöhen

**Buchdeckung**:
- ✅ Kap. 04: VR-Training für gefährliche Umgebungen wissenschaftlich belegt
- ✅ Kap. 07: Motion Sickness als Adoptionshemmnis
- ⚠️ Kap. 03: ROI für Safety-Training (Unfallvermeidungskosten) nicht explizit kalkuliert
- ❌ Windenergie als Branche: kein Beispiel, keine Spezifik
- ❌ Zertifizierung und Dokumentationspflicht von VR-Trainings: nicht thematisiert
- ❌ Offshore-Besonderheiten (Seekrankheit, Netzinfrastruktur): nicht abgedeckt

---

## Fall 13 — Rechtsanwaltskanzlei (Arbeits- und Gesellschaftsrecht)

**Profil**: Anwaltsbüro, 6 Rechtsanwälte + 4 Assistenz, Lübeck. Schwerpunkt: Arbeitsrecht, Gesellschaftsrecht, M&A-Beratung für Mittelstand.

**VR-Frage**: „Können wir vertrauliche Mandantengespräche oder Mediationen in VR führen — insbesondere wenn Parteien weit entfernt sind?"

**Kernbedürfnis**: Fernmandantschaft effektiver bedienen; Verhandlungseffektivität erhöhen; Reisekosten für Mandanten senken.

**Besonderheiten**:
- **Anwaltliches Berufsgeheimnis (§ 43a BRAO)**: absolutes Verbot der unkontrollierten Datenverarbeitung durch Dritte
- Meta Quest vollständig inakzeptabel — sprachliche Metadaten, Raumerfassung (Passthrough) würden prozessual relevante Informationen exponieren
- Berufsrechtliche Sanktionen bei Datenschutzverstoß: bis zur Kanzleizulassungsversagung
- VR für Mediation: nonverbale Kommunikation in Konfliktsituationen — Forschungsstand?
- Richter/Gerichte als Dritte in VR: technisch/rechtlich kaum vorstellbar (derzeit)

**Buchdeckung**:
- ⚠️ Kap. 05: Bailenson (2021) — nonverbale Kommunikation in VR für Verhandlungen relevant
- ❌ **Anwaltliches Berufsgeheimnis + VR**: komplett fehlend — kritische Lücke für SH-Zielgruppe
- ❌ Mediation in VR: kein Beispiel, kein Forschungsstand
- ❌ Rechtsrahmen für VR-Gespräche (Beweiswert, Identifizierung): nicht thematisiert

---

## Fall 14 — Logistik- und Speditionsunternehmen

**Profil**: GmbH, 65 Mitarbeitende, Lübeck. Lagerlogistik, LKW-Spedition, Umschlag. Kunden: Lebensmitteleinzelhandel und Industriegüter.

**VR-Frage**: „Können wir unsere Staplerfahrer und Lageristen in Sicherheitsregeln und Notfallprozeduren einweisen, ohne den Betrieb zu unterbrechen?"

**Kernbedürfnis**: Unfallvermeidung; Compliance mit BGW/BG-Vorschriften; Einarbeitung Zeitarbeitskräfte.

**Besonderheiten**:
- Hohes Unfallrisiko (Gabelstapler): Trainingsdefizite haben direkte Haftungsfolgen
- Zeitarbeitskräfte: schnelle, standardisierte Einweisung notwendig
- Berufsgenossenschaft (BG Handel und Warenlogistik): Nachweis der Unterweisung
- Lager ist WLAN-abgedeckt; IT-Infrastruktur vorhanden
- Datenschutz: Mitarbeiterdaten im Schichtbetrieb (Betriebsrat involviert)

**Buchdeckung**:
- ✅ Kap. 04: VR-Training für Sicherheitsverfahren belegt
- ✅ Kap. 03: Kostenreduktion durch VR-Schulung vs. externe Schulungsanbieter
- ⚠️ Kap. 08: Betriebsrat und Mitbestimmung bei VR-Einführung: nicht thematisiert
- ❌ Berufsgenossenschaft als Zertifizierungsinstanz: nicht erwähnt
- ❌ Betriebsrat und Mitbestimmungsrecht § 87 BetrVG bei VR-Überwachung: kritische Lücke
- ❌ Zeitarbeit und VR-Onboarding: nicht spezifisch behandelt

---

## Fall 15 — Einzelhandel (Einrichtungshaus, inhabergeführt)

**Profil**: Einzelbetrieb, 12 Mitarbeitende, Flensburg Innenstadt. Möbel und Wohnaccessoires, Mittelpreissegment. Unter Druck durch Online-Handel.

**VR-Frage**: „Können wir Kunden eine VR-Wohnraumvisualisierung anbieten, damit sie sich besser vorstellen, wie ein Sofa bei ihnen zu Hause aussieht?"

**Kernbedürfnis**: Kaufentscheidung erleichtern; Retouren reduzieren; Erlebniskauf als USP vs. Amazon.

**Besonderheiten**:
- Kein IT-Personal; Lösungen müssen plug-and-play sein
- Kunden stehen im Laden — kurze Session (<5 Min), kein Sitzen möglich
- Meta Quest für Kundenkontakt: Kundendaten-Problematik (s. Fall 01)
- Kleines Budget; Miet-/Abonnement-Modelle bevorzugt
- IKEA Place (AR) als direkter Wettbewerber bereits kostenlos verfügbar

**Buchdeckung**:
- ✅ Kap. 03: IKEA Place als Praxisbeispiel (Customer Experience)
- ✅ Kap. 04: Produktkonfiguration als VR-Typ
- ⚠️ Kap. 07: Stehende Kurznutzung für VR-Erstnutzer: Motion-Sickness-Risiko erwähnt, aber Stehen nicht spezifisch
- ❌ AR als Alternative/Ergänzung zu VR für kurze Kundenerlebnisse: systematische Abgrenzung fehlt
- ❌ Wettbewerbsvergleich VR vs. AR für Möbel/Einrichtung: nicht durchgeführt

---

## Fall 16 — Grenzregion-Handelsunternehmen (Deutsch-Dänisch)

**Profil**: GmbH, 28 Mitarbeitende, Sitz Flensburg, Niederlassung Aarhus (DK). Import/Export, Handelsvertretungen. Wöchentliche Meetings zwischen DE- und DK-Teams.

**VR-Frage**: „Können wir unsere Montags-Meetings zwischen Flensburg und Aarhus in VR statt in Zoom abhalten — und dabei das Gefühl echter Zusammenarbeit zurückbringen?"

**Kernbedürfnis**: Teamkohäsion in verteiltem Team; nonverbale Kommunikation wiedergewinnen; Reisekosten senken.

**Besonderheiten**:
- **Kernzielgruppe des Projekts**: DK-DE-Grenzregion als geografischer Fokus
- Sprachenwechsel DE/DK mitten im Meeting: VR-Plattform muss Mehrsprachigkeit unterstützen
- Dänische DSGVO-Interpretation: kongruent mit EU-DSGVO, aber dänische Datenschutzbehörde (Datatilsynet) eigene Praxis
- Kulturelle Kommunikationsunterschiede DK-DE: Mascarenhas (2019) direkt relevant
- Mitarbeitende in DK und DE: unterschiedliche ATI-Verteilungen möglich

**Buchdeckung**:
- ✅ Kap. 07: Mascarenhas (2019) — kulturelle Kommunikationsunterschiede in VR
- ✅ Kap. 04: Remote-Meeting als VR-Anwendungsfall (Horizon Workrooms, Microsoft Mesh)
- ✅ Kap. 05: UTAUT Social Influence als Adoptionsfaktor
- ⚠️ Kap. 06: Eigene Verhandlungsstudie — Übertragbarkeit auf bikulturelles Team nicht explizit
- ❌ Datatilsynet (DK) und Interoperabilität mit deutschen DSGVO-Anforderungen: nicht thematisiert
- ❌ Mehrsprachige VR-Meetings (Sprach-/Textübersetzung in Echtzeit): nicht beschrieben

---

## Fall 17 — IT-Systemhaus

**Profil**: GmbH, 32 Mitarbeitende, Kiel. IT-Infrastruktur, Managed Services, Microsoft-Partner. Kunden: SH-KMU.

**VR-Frage**: „Können wir unseren KMU-Kunden VR als Managed Service anbieten — und was müssen wir dabei technisch und rechtlich beachten?"

**Kernbedürfnis**: Neues Geschäftsfeld; Differenzierung vom Commodity-IT-Geschäft; VR-Kompetenz als Alleinstellungsmerkmal in SH.

**Besonderheiten**:
- Systemhaus versteht die Technologie — die Frage ist Marktgröße und Lizenzmodelle
- Haftung als Dienstleister bei Datenpannen in KMU-VR-Umgebungen
- Microsoft Mesh als naheliegende Lösung (sind Microsoft-Partner): Teams-Integration
- VR-Hardware-Beschaffung, Lagerung, Wartung als Service: Logistikfrage
- DSGVO-Beratungspflicht gegenüber Kunden bei VR-Einführung

**Buchdeckung**:
- ✅ Kap. 04: Microsoft Mesh als Marktprodukt mit Teams-Integration dokumentiert
- ✅ Kap. 08: Technische Implementierungsebene detailliert
- ⚠️ Kap. 03: Geschäftsmodell „VR als Service" nicht explizit behandelt
- ❌ VR-Managed-Service-Modell (Hardware-as-a-Service, Software-Lizenzmodelle): fehlend
- ❌ Haftung des IT-Dienstleisters bei VR-Datenschutzverstößen: nicht thematisiert

---

## Fall 18 — Zahnarztpraxis (Schwerpunkt Angstpatienten)

**Profil**: Einzelpraxis, 6 Mitarbeitende, Neumünster. Allgemeinzahnmedizin, beworbener Schwerpunkt Angstpatienten, Lachgassedierung.

**VR-Frage**: „Können wir VR-Ablenkung während der Behandlung anbieten, um Angstpatienten zu beruhigen — und ist das medizinisch seriös?"

**Kernbedürfnis**: Patientenzufriedenheit; Differenzierung; weniger Abbrüche bei Angstpatienten.

**Besonderheiten**:
- **Medizinprodukteverordnung (MDR)**: VR als therapeutisches Mittel unterliegt ggf. der MDR
- Patientendaten: absolute ärztliche Schweigepflicht; Meta Quest vollständig inakzeptabel
- Infektionshygiene: Headset muss zwischen Patienten desinfiziert werden; wechselbare Hygienemasken
- Zahnbehandlungsposition (liegend, Mund geöffnet): Controller-Bedienung unmöglich — passive VR
- Lachgas + VR: Wechselwirkungen bei Immersion und Orientierung unbekannt

**Buchdeckung**:
- ⚠️ Kap. 07: VR-Sickness und körperliche Reaktionen, aber Liegendposition nicht spezifisch
- ❌ Medizinische VR-Anwendungen und MDR: komplett fehlend
- ❌ Hygiene-Protokolle für Headsets: nicht thematisiert
- ❌ Passive VR-Erlebnisse (kein Controller): nicht als Anwendungsklasse beschrieben
- ❌ Ärztliche Schweigepflicht + VR-Datenschutz: nicht abgedeckt

---

## Fall 19 — Seeschifffahrts-/Hafenunternehmen

**Profil**: GmbH, 55 Mitarbeitende, Kiel. Hafendienstleistungen, Schlepperoperationen, kleinere Küstenschifffahrt. Stark regulierte Branche (SOLAS, STCW).

**VR-Frage**: „Können maritime Pflichtschulungen (Feuerschutz, Rettungsboote, MOB-Manöver) teilweise durch zertifizierte VR-Simulationen abgedeckt werden — und werden diese von Klassifikationsgesellschaften anerkannt?"

**Kernbedürfnis**: Compliance sicherstellen; Kosten für physische Simulatoren (sehr teuer) reduzieren; Dokumentation vereinfachen.

**Besonderheiten**:
- STCW-Zertifizierung: Pflichttrainings müssen von anerkannten Einrichtungen abgenommen werden
- Klassifikationsgesellschaften (Lloyd's, DNV, Bureau Veritas): erkennen VR-Simulatoren nur unter bestimmten Bedingungen an
- Seekrankheitsanfälligkeit der Besatzung kann bei VR-Training relevant sein
- Hochsicherheitsrelevant: Fehler auf See können Katastrophen auslösen
- Internationales Recht: IMO-Vorgaben überlagern nationale Datenschutzregeln

**Buchdeckung**:
- ✅ Kap. 04: Safety-Training in VR allgemein belegt
- ❌ Maritime Regulierung (STCW, SOLAS, IMO) und VR-Zertifizierung: komplett fehlend
- ❌ Klassifikationsgesellschaften als Zertifizierungsinstanz: nicht erwähnt
- ❌ Nautische VR-Simulatoren als Marktprodukt: kein Beispiel
- ❌ Seekrankheit vs. Motion Sickness in VR — Überlappung: nicht thematisiert

---

## Fall 20 — Kreativagentur / Designstudio

**Profil**: GbR, 5 Mitarbeitende, Flensburg. Corporate Design, Webentwicklung, 3D-Visualisierungen für regionale Unternehmen. Junges Team (Ø 29 Jahre).

**VR-Frage**: „Wir wollen selbst VR-Inhalte anbieten — welche Technologieentscheidungen sind jetzt strategisch richtig, damit wir nicht in drei Jahren auf der falschen Plattform sind?"

**Kernbedürfnis**: Geschäftsfeldentwicklung; Technologie-Roadmap; welche Tools/Plattformen haben Zukunft?

**Besonderheiten**:
- Hohes technisches Grundverständnis; sehr hohe ATI
- Budget für Investitionen begrenzt (GbR-Struktur)
- Frage der Plattformwahl: Meta vs. Apple Vision Pro vs. WebXR vs. OpenXR
- Kundenseitig: SH-KMU als Auftraggeber → Entscheidungen der Kunden beeinflussen die Agentur
- DSGVO: Eigene Produktionen müssen datenschutzkonform für Kundenübergabe sein

**Buchdeckung**:
- ✅ Kap. 08: OpenXR als plattformübergreifender Standard empfohlen
- ✅ Kap. 09: Apple Vision Pro, technologische Trends
- ✅ Kap. 08: Unity + Meta SDK als Referenz (eigener Workshop)
- ⚠️ Kap. 09: Plattformwahl-Empfehlung für Technologieentscheider: zu allgemein
- ❌ WebXR als Plattform für Agenturen ohne native App-Entwicklung: nicht detailliert genug
- ❌ Strategische Plattformwahl-Matrix (Meta vs. Apple vs. WebXR): kein Entscheidungsrahmen

---

## Zusammenfassung: Buchdeckungsmatrix

| Themenbereich | Abgedeckt? | Beispiel-Fälle |
|---|---|---|
| VR-Training für prozedurale Skills | ✅ gut | F02, F05, F11, F12, F14 |
| Kundenpräsentation / Produktvisualisierung | ✅ gut | F01, F04, F09, F15 |
| Remote-Meeting / Kollaboration | ✅ gut | F08, F13, F16 |
| Kosten-Nutzen / ROI | ⚠️ teilweise | F01, F04, F12 |
| Datenschutz / Meta DSGVO | ❌ kritische Lücke | F06, F08, F13, F18 |
| Berufsgeheimnisse (Anwalt, Arzt, Steuer) | ❌ kritische Lücke | F08, F13, F18 |
| LIDAR-Scanning und 360°-Fotografie | ❌ Experiment fehlt | F03 |
| Eigene Feldexperimente (Messe, Boot) | ❌ nicht eingearbeitet | F03, F07 |
| Maritime / STCW-Zertifizierung | ❌ fehlend | F19 |
| Betriebsrat / Mitbestimmung § 87 BetrVG | ❌ fehlend | F14 |
| Mehrsprachige VR-Inhalte | ❌ fehlend | F02, F05, F16 |
| Hygiene (Headset-Sharing) | ❌ fehlend | F11, F18 |
| Agrar / Saisonkräfte | ❌ fehlend | F05 |
| Healthcare / Medizinrecht (MDR) | ❌ fehlend | F06, F18 |
| VR als Dienstleistungsgeschäftsmodell | ❌ fehlend | F07, F17 |
| SH-spezifisch: ULD, Förderung, Branche | ❌ fehlend | alle |
| Öffentliche Beschaffung | ❌ fehlend | F11 |
| Plattformwahl-Matrix | ⚠️ teilweise | F20 |

---

## Priorisierte Lücken für nächste Schritte

### Kritisch (direkt buchrelevant, sofort schließen)

1. **Meta Quest DSGVO-Inkompatibilität** — explizites Kapitel oder Einschub in Kap. 08; ULD SH als Referenz
2. **Berufsgeheimnisrelevante Kontexte** — Einschub in Kap. 08; DSGVO-konforme Alternativen
3. **Eigene Feldexperimente einarbeiten** — F03 (360°/LIDAR), F07 (Messestand) als Kap. 06-Erweiterung
4. **Betriebsrat / § 87 BetrVG** — Einschub in Kap. 03 oder Kap. 10

### Wichtig (nächste Buchversion)

5. **Mehrsprachige VR-Inhalte** — Kap. 04 oder Kap. 07
6. **Hygiene-Konzept Headset-Sharing** — Kap. 08
7. **SH-spezifische Förderprogramme** — Kap. 03 oder neuer Anhang
8. **VR als Dienstleistungsmodell** — Kap. 03 (Geschäftsmodell-Variante)

### Für spätere Experimente / Vertiefungen

9. **Maritime Regulierung** (STCW, Klassifikationsgesellschaften)
10. **Medizinrecht (MDR) für therapeutische VR**
11. **Zertifizierungsrahmen für VR-Trainings** (BG, STCW, ISO)
