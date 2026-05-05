# Entwurf: LIDAR-Scanning mit Consumer-Hardware

> **Zielstelle im Buch:** `Buch/06_empirische_untersuchung.md`
> Einzufügen als neuer Abschnitt **nach** dem bestehenden Abschnitt „Verhaltensbeobachtung (CIPD-Kodierung)",
> vor einem ggf. folgenden Abschnitt zu Experiment H2 (360°-Fotografie).
> Überschriftenebene: `##` (gleichwertig mit „Studiendesign", „Ergebnisse" etc.)
>
> **Framework-Verortung:** TI (Datenerfassung), VA (VR-Eignung für Raumanalyse-Meetings)
> **Testfall-Relevanz:** F03 (Sportbootgutachter), F09 (Architekturbüro), F04 (Maschinenbauer)

---

## Praxisexperiment H1: LIDAR-Scanning mit Consumer-Hardware (Negativbefund)

### Zielsetzung und Versuchsaufbau

Im Rahmen des Projekts wurde erprobt, ob sich handelsübliche Consumer-Hardware für die Erstellung VR-tauglicher 3D-Scans eignet. Konkret interessierten zwei Anwendungsszenarien:

1. **Virtuelle Produktvorstellung** — dreidimensionale Darstellung einzelner Gegenstände für Remote-Demonstrations- oder Verkaufsgespräche in VR
2. **Virtuelle Gebäudetour** — begehbare Nachbildung von Büro- oder Arbeitsräumen für Besichtigungen, Planung oder Einweisungen über Distanz

Als Hardware dienten zwei **iPhone 15 Pro** mit dem integrierten LIDAR-Scanner; als Software wurde die **3D Scanner App** (Apple App Store) eingesetzt, die für Endanwender eine einfache Point-and-Shoot-Erfahrung verspricht.

Die Versuchsobjekte umfassten zwei Kategorien:

| Kategorie | Beispiele |
|-----------|-----------|
| Kleine Alltagsgegenstände | Tasse, Glas, Kugelschreiber, Stiftehalter (Gitterstruktur), Rubber Duck, Telefonhörer |
| Büroräume | Verschiedene Innenräume, 5–20 m² |

Die Wahl dieser Bandbreite sollte klären, ob die Technologie für kleinskalige Objekte (Produktdemonstration) und raumgroße Umgebungen (Gebäudetour) gleichermaßen funktioniert.

### Beobachtungen und Probleme

Die Versuche zeigten in beiden Kategorien erhebliche Qualitätsmängel, die einem direkt verwendbaren Ergebnis entgegenstanden:

**Kleine Gegenstände:**

- **Detailverlust**: Feine Strukturen — etwa die Gitterstruktur eines Stiftehalters oder beschriftete Oberflächen — wurden unzureichend aufgelöst. Das Scannraster der LIDAR-Sensortechnologie in Smartphones ist für solche Feinstrukturen zu grob.
- **Konkave Formen und Hohlräume**: Stark konkave Geometrien stellten den Scanner vor grundlegende Probleme. Das Innere einer Tasse, der Henkel oder ähnliche enge Hohlräume wurden entweder gar nicht erfasst oder mit starken Artefakten gefüllt. Der LIDAR-Sensor kann von einer Position aus keine Flächen einsehen, die sich „hinter" einer Kante befinden — ein physikalisches Limit, das durch Kamerabewegung nur teilweise kompensiert werden kann.

**Büroräume:**

- **Möbelqualität**: Tische, Stühle und andere Einrichtungsgegenstände wurden mit deutlich sichtbaren Artefakten und unvollständigen Flächen gescannt. Die resultierende Darstellung wirkte wenig glaubwürdig und war für professionelle Präsentationszwecke nicht geeignet.
- **Scanaufwand und -dauer**: Ein halbwegs ordentlicher Raum-Scan erforderte eine sorgfältige, gleichmäßige Kamerabewegung über mehrere Minuten. Selbst bei gewissenhafter Durchführung blieben Qualitätsmängel bestehen. Für eine spontane oder nicht technisch geschulte Nutzung ist der Aufwand zu hoch.

**Generelle Probleme (kategorieübergreifend):**

- **Loch-Artefakte**: An geometrisch komplexen oder reflektierenden Stellen entstanden im rekonstruierten Mesh sichtbare Löcher und Fehlstellen, die ohne manuelle Nachbearbeitung in einer 3D-Modellierungssoftware nicht zu schließen sind. Betroffen waren sowohl glänzende Kunststoffoberflächen bei Objekten als auch Übergangsbereiche zwischen Wand und Boden in Räumen.
- **Transparenz**: Glasflächen wurden vom LIDAR-Sensor systematisch falsch oder gar nicht erfasst. Glasscheiben in Büroräumen (Fenster, Trennwände) sowie transparente Behälter wie Trinkgläser oder Trinkflaschen wurden entweder überhaupt nicht als Objekt registriert oder als undurchsichtige, artefaktbehaftete Fläche rekonstruiert. Da LIDAR auf reflektiertem Infrarotlicht basiert, durchdringt der Strahl transparente Materialien, anstatt von ihnen zurückgeworfen zu werden — ein grundlegendes physikalisches Problem, das softwareseitig nicht lösbar ist.

In beiden Kategorien wäre zusätzliche Nachbearbeitung in einer 3D-Modellierungssoftware (z. B. Blender, Meshmixer) erforderlich gewesen, um VR-taugliche Ergebnisse zu erzielen. Damit war die zentrale Prämisse des Experiments — die Technologie soll einfach und von Nicht-Spezialisten nutzbar sein — nicht erfüllt.

### Einordnung und Handlungsempfehlung

Das Experiment bestätigt, dass LIDAR-gestütztes 3D-Scanning auf Consumer-Smartphones im Jahr 2025/2026 noch nicht den Reifegrad erreicht hat, der für einen direkten Einsatz in professionellen VR-Anwendungen erforderlich wäre. Die Technologie ist für grobe Raumerfassung (z. B. Grundrissmessung mit Apps wie Canvas) durchaus brauchbar, scheitert jedoch an den Qualitätsanforderungen für immersive VR-Erlebnisse.

**Für KMU-Entscheider:** LIDAR-Scanning mit Smartphones ist derzeit **nicht als niedrigschwelliger Einstiegsweg** in die virtuelle Produktpräsentation oder Gebäudetour zu empfehlen. Wer diesen Weg gehen möchte, benötigt entweder:

- **Dedizierte Photogrammetrie-Software** (z. B. RealityCapture, Metashape) mit mehreren hundert Einzelfotos — höhere Qualität, aber erheblich aufwändiger, oder
- **Professionelle 3D-Scan-Dienstleister** mit Faro-Scanner oder vergleichbarer Hardware — deutlich höheres Budget, aber direkt verwertbare Ergebnisse.

Eine erneute Evaluierung der Consumer-LIDAR-Qualität empfiehlt sich, sobald Apple oder Drittanbieter die Rekonstruktions-Algorithmen signifikant verbessern — die Hardware-Grundlage (LIDAR-Chip) ist vorhanden; der limitierende Faktor ist die Software.

> **Methodische Transparenz:** Dieses Experiment lieferte ein negatives Ergebnis. Negative Befunde sind für den Erkenntnisgewinn ebenso wertvoll wie positive: Sie verhindern, dass KMU Ressourcen in einen Ansatz investieren, der unter Praxisbedingungen nicht funktioniert.

---

### Aussicht: LiDAR als Enabler für Gaussian Splatting

Die oben beschriebenen Qualitätsgrenzen des reinen LiDAR-Scannens beziehen sich auf einen spezifischen Workflow: direkter Scan → 3D-Mesh → VR. Ein technologischer Paradigmenwechsel, der sich seit 2023 abzeichnet und 2025/26 in die Praxis diffundiert, verändert diese Einschätzung grundlegend: **3D Gaussian Splatting (3DGS)** — ein KI-gestütztes Verfahren zur volumetrischen Rekonstruktion von Szenen aus Videomaterial.

**Das Zusammenspiel: LiDAR als Gerüst, 3DGS als Hülle**

Entscheidend ist, dass LiDAR und Gaussian Splatting nicht Alternativen, sondern Komplementärtechnologien sind. Der LiDAR-Sensor übernimmt dabei die Rolle eines unsichtbaren Rohbau-Gerüsts:

1. **Initialisierung der Punktwolke.** Ohne LiDAR muss ein 3DGS-Algorithmus die räumliche Struktur einer Szene durch *Structure from Motion* (SfM) mühsam aus zweidimensionalen Videobildern errechnen — ein rechenintensiver Prozess. Der LiDAR-Sensor liefert dem Algorithmus sofort eine fertige, grobe 3D-Punktwolke (*Point Cloud Prior*), auf deren Basis das eigentliche Splatting-Training unmittelbar beginnen kann.

2. **Absolute Maßstabstreue.** Reines Videomaterial hat kein intrinsisches Größengefühl — ein KI-Algorithmus kann nicht unterscheiden, ob er ein Spielzeugauto aus wenigen Zentimetern oder einen echten PKW aus fünf Metern betrachtet. LiDAR liefert millimetergenaue Tiefeninformationen; die fertige 3D-Szene ist damit direkt maßstabsgetreu und für Anwendungen nutzbar, in denen reale Abstände messbar sein müssen (Immobilien, Fertigung, Set-Planung).

3. **Robustheit bei strukturlosen Flächen.** Kamerabasierte Rekonstruktionsverfahren versagen an kontrastarmen Flächen — weißer Raufasertapete, spiegelnden Fenstern, uniformen Decken. Der LiDAR-Laser erfasst diese Geometrien physikalisch, unabhängig von ihrer optischen Textur, und gibt dem Algorithmus den notwendigen Anker.

Wo die reine LiDAR-Rekonstruktion an Auflösungs- und Reichweitengrenzen stößt (ca. 5 Meter, grobmaschige Meshes), tritt 3DGS in die Lücke: Es nutzt das physikalisch korrekte LiDAR-Gerüst und legt die hochauflösenden Bilddaten der Smartphone-Kamera (48 Megapixel) fehlerfrei darüber. Das Ergebnis vereint geometrische Präzision mit fotorealistischer Texturierung.

**Aktuelle Entwicklungen (Stand: Frühjahr 2026)**

Die Technologiereife hat einen Punkt erreicht, an dem relevante kommerzielle Anwendungen entstehen:

| Entwicklung | Bedeutung für KMU |
|-------------|-------------------|
| **4D Gaussian Splatting** (Zeitdimension) — A$AP Rockys Musikvideo „Helicopter" (2025) wurde mit 56 Kameras aufgenommen und als 4D-Splat rekonstruiert; nachträgliche Kamerafahrten durch die Szene wurden damit möglich. | Zeigt die Richtung für dynamische Produktdemonstrationen und Event-Dokumentation. |
| **Zillow SkyTour** (März 2026) — das US-Immobilienportal wandelt Drohnenvideos vollautomatisch in interaktive, volumetrische 3D-Gebäudeszenen um, durch die Nutzer stufenlos zoomen können. | Direktes Vorbild für virtuelle Immobilienpräsentationen und Betriebsbesichtigungen im KMU-Kontext. |
| **iPhone-Rig bei Radiant Images (NAB, April 2026)** — 24 handelsübliche iPhones ersetzen aufwändige „Bullet-Time"-Rigs; Gaussian Splatting erzeugt eine vollständig navigierbare 3D-Szene, in der Brennweite und Perspektive im Nachhinein frei wählbar sind. | Demonstriert, dass Hollywood-Technik mit Consumer-Hardware erreichbar wird. |
| **V-Ray 7 mit nativer 3DGS-Unterstützung** (Anfang 2026) — der weit verbreitete Industrie-Renderer integriert Gaussian Splatting nativ; reale Umgebungen lassen sich nahtlos mit computergenerierten Objekten kombinieren. | Ermöglicht die Einbettung gescannter Realräume in bestehende 3D-Produktions-Workflows. |
| **Consumer-Apps wie Splat Studio** — Nutzer erstellen aus simplen Handyvideos begehbare 3D-„Dioramen" ohne technisches Vorwissen. | Niedrigschwelliger Einstiegspunkt: Pilotprojekte ohne Spezialisten-Know-how möglich. |

**Handlungsempfehlung (aktualisiert)**

Der Negativbefund zum direkten LiDAR-Mesh-Workflow bleibt gültig. Die Kombination *LiDAR-gestützte Videokamera + 3D Gaussian Splatting* stellt jedoch einen qualitativ anderen Ansatz dar, der die beschriebenen Limitierungen strukturell adressiert. Für KMU-Entscheider, die den Einstieg in die virtuelle Produkt- oder Raumdarstellung prüfen, empfiehlt sich:

- **Kurzfristig (2026):** Consumer-Apps auf 3DGS-Basis testen (z. B. Splat Studio, Luma AI); Hardwarebasis iPhone 15 Pro oder neuer ist ausreichend.
- **Mittelfristig:** Professionelle Dienste evaluieren, die automatisiert aus Drohnen- oder Handyvideo volumetrische 3D-Szenen erzeugen (vergleichbar mit Zillow SkyTour).
- **Längerfristig:** Sobald 3DGS in Standard-Renderingpipelines etabliert ist (V-Ray 7 ist ein Indikator), wird die Technologie voraussichtlich als Selbstverständlichkeit in Visualisierungs-Workflows eingehen.

Eine erneute Evaluierung des Gesamtworkflows (LiDAR + 3DGS) im Rahmen dieses Projekts ist für 2026/27 vorgesehen.