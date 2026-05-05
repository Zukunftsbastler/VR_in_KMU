# Entwurf: 360°-Fotografie als VR-Erlebnis (Fallstudie Sportbootgutachten)

> **Zielstelle im Buch:** `Buch/06_empirische_untersuchung.md`
> Einzufügen als neuer Abschnitt **nach** H1 (LIDAR-Scanning, Negativbefund),
> als direkt anschließendes Praxisexperiment H2.
> Überschriftenebene: `##` (gleichwertig mit H1)
>
> **Framework-Verortung:** TI (Datenerfassung), VA (VR-Eignung für Besichtigungs- und Begutachtungsszenarien)
> **Testfall-Relevanz:** F03 (Sportbootgutachter)
>
> **⚠️ Offene Punkte — vor Fertigstellung zu klären:**
> - Einverständnis Stefan Bruns / sportboot-gutachter.de zur namentlichen Nennung
> - Anzahl der fotografierten Boote / Umfang der Bildserie
> - Ergebnisse der Nutzertests oder Praxiseinsätze (sofern vorhanden)
> - Bewertung des Ansatzes durch den Auftraggeber / Gutachter
> - Technische Details zur Unity-Projektversion und eingesetzten VR-Hardware

---

## Praxisexperiment H2: 360°-Fotografie als immersive Bootsinspektion

### Zielsetzung und Versuchsaufbau

Als Gegenansatz zum aufwändigen LIDAR-basierten 3D-Scanning (→ H1) wurde erprobt, ob sich **sphärische 360°-Fotografie** als niedrigschwellige Alternative für immersive Besichtigungs- und Begutachtungsszenarien eignet. Konkret stand die Frage im Mittelpunkt, ob ein Gutachter oder Käufer ein Wasserfahrzeug in VR so vollständig inspizieren kann, dass der Gang zum physischen Objekt zumindest für eine Vorabprüfung entbehrlich wird.

Als Pilotobjekt diente das Motorboot **„Albin Köbis"**. Aufnahmen wurden mit einer **Insta360**-Kamera erstellt, die in einem einzigen Auslösevorgang eine vollständige Rundumsicht (equirektangulares Bild, 360° × 180°) erfasst.

### Technische Umsetzung in Unity

Die erstellten 360°-Aufnahmen wurden als Grundlage für eine Unity-VR-Applikation genutzt:

**Skybox-Integration:**
Die equirektangularen Bilder wurden als **Skybox** in Unity eingebunden. Damit umgibt das Foto den Betrachter vollständig — er steht virtuell am Aufnahmeort des Fotos und blickt in alle Richtungen, ohne dass eine aufwändige 3D-Modellierung des Bootes erforderlich ist.

**Points of Interest (POI):**
Innerhalb der VR-Umgebung konnten **Points of Interest** im 360°-Bild platziert werden. Jeder POI enthält weiterführende Informationen zu einem definierten Bereich des Bildes — z. B. technische Details, Zustandsbeschreibungen oder Bewertungen relevanter Bauteile. Der Gutachter kann damit sein Fachwissen strukturiert im Bildraum verankern.

**Navigation:**
Zwischen mehreren Aufnahmepositionen (z. B. Cockpit, Vorschiff, Maschinenraum) wurde eine **Controller-gestützte Navigation** implementiert, die konzeptionell Google Street View nachempfunden ist: Der Nutzer wählt per VR-Controller einen Navigationspunkt im Bild und wechselt damit zur nächsten Aufnahmeposition. Das Ergebnis ist ein sequenzieller, benutzergesteuerter Rundgang durch das Fahrzeug.

### Offene Punkte (noch zu ergänzen)

- Anzahl der Aufnahmepositionen an der „Albin Köbis"
- Eingesetzte VR-Hardware beim Test (z. B. Meta Quest 2/3, PC-VR)
- Durchgeführte Nutzertests: Teilnehmer, Setting, Beobachtungen
- Qualitative oder quantitative Ergebnisse (Akzeptanz, wahrgenommener Nutzen, Grenzen)
- Vergleich mit physischer Inspektion: Zeitaufwand, Erkenntnisqualität
- Skalierbarkeit: Eignung für weitere Bootstypen oder andere Fahrzeugkategorien
- Reaktion / Bewertung durch Stefan Bruns (sportboot-gutachter.de)

### Vorläufige Einordnung

Der Ansatz adressiert direkt die Schwäche, die H1 (LIDAR) aufgedeckt hat: Anstatt ein aufwändiges 3D-Modell zu erzeugen, wird die Realität fotografisch konserviert. Die 360°-Fotografie ist mit handelsüblicher Consumer-Hardware (Insta360-Kamera) und ohne technisches Vorwissen durchführbar. Die Qualität des resultierenden VR-Erlebnisses hängt primär von der Bildauflösung der Kamera und der Anzahl der Aufnahmepositionen ab — nicht von Rekonstruktionsalgorithmen.

Für Besichtigungs- und Begutachtungsszenarien, bei denen die visuelle Dokumentation eines realen Zustands im Vordergrund steht (z. B. Bootsinspektion, Immobilienbewertung, Maschinenzustand), bietet dieser Ansatz einen deutlich direkteren Weg zur VR-Integration als polygonbasiertes 3D-Scanning.

> **Methodische Transparenz:** Die inhaltliche Bewertung dieses Experiments (Stärken, Grenzen, Übertragbarkeit) ist zum aktuellen Zeitpunkt noch offen und wird nach Vorliegen der Nutzerdaten ergänzt.
