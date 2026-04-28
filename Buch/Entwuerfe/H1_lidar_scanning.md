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


##### 

Kurz gesagt: Der LiDAR-Scanner des iPhones (verfügbar in den Pro-Modellen) ist nicht zwingend notwendig für Gaussian Splatting, aber er fungiert als massiver Turbo und Präzisions-Anker für den gesamten Prozess.

Man kann sich das Zusammenspiel wie beim Hausbau vorstellen: Der LiDAR-Sensor baut in Sekundenschnelle das unsichtbare Rohbau-Gerüst, und das Gaussian Splatting gießt die hochauflösenden, fotorealistischen Details (die Texturen und Beleuchtung aus der normalen Kamera) darüber.

Hier ist im Detail, welche Rolle LiDAR dabei spielt:

1. Der Kickstart für die KI (Die initiale Punktwolke)

Bevor der Algorithmus für das Gaussian Splatting beginnen kann, die Millionen von "Splats" zu optimieren, muss er wissen, wo sich die Kamera im Raum befand und wie der Raum grob aussieht.

Ohne LiDAR: Die Software muss diese Daten durch einen rechenintensiven Prozess namens Structure from Motion (SfM) erst mühsam aus den 2D-Videobildern errechnen. Das dauert oft sehr lange.

Mit LiDAR: Der Sensor wirft ohnehin Infrarot-Punkte in den Raum und misst deren Reflexion. Er liefert dem Algorithmus also sofort eine fertige, wenngleich grobe 3D-Punktwolke ("Point Cloud Prior"). Die KI kann dadurch sofort mit dem eigentlichen Splatting-Training beginnen, was den Prozess enorm beschleunigt.

2. Der echte Maßstab (Absolute Skalierung)

Ein reines Video hat kein Gefühl für Größe. Eine KI kann oft nicht unterscheiden, ob sie gerade ein kleines Spielzeugauto aus fünf Zentimetern Entfernung oder einen echten SUV aus fünf Metern Entfernung betrachtet. LiDAR liefert absolute, millimetergenaue Tiefeninformationen. Das bedeutet, dass die fertige 3D-Szene direkt maßstabsgetreu ist. Das ist entscheidend für Anwendungen wie Immobilien (Zillow) oder Set-Planung im Film, wo man in der fertigen 3D-Szene reale Abstände messen möchte.

3. Die Rettung bei strukturlosen Flächen

Kamera-basierte Photogrammetrie verlässt sich auf Kontraste und Muster. Eine komplett glatte, weiße Raufasertapete oder ein spiegelndes Fenster bringen traditionelle Algorithmen zum Verzweifeln, da sie keine Referenzpunkte finden. Der LiDAR-Laser tastet die Wand physisch ab, unabhängig von ihrer Farbe oder Textur. Er sagt der Software: "Hier ist eine solide Wand, auch wenn sie auf dem Video nur wie eine weiße Fläche aussieht."

Warum LiDAR allein nicht reicht (und 3DGS übernimmt)

Man könnte sich fragen: Wenn das iPhone LiDAR hat, wozu brauche ich dann noch Gaussian Splatting? Die Antwort liegt in der Auflösung. Die reinen LiDAR-Scans von iPhones (wie man sie aus älteren Scan-Apps kennt) sehen oft aus wie geschmolzene, grobmaschige Videospiel-Grafiken aus den frühen 2000ern. Der Sensor hat eine begrenzte Reichweite (ca. 5 Meter) und eine relativ geringe Auflösung.

Genau hier greift das Gaussian Splatting ein: Es nutzt das grobe, aber physikalisch korrekte LiDAR-Gerüst, um die ultra-hochauflösenden Bilddaten der 48-Megapixel-Hauptkamera des iPhones fehlerfrei darüberzulegen. Das Ergebnis vereint die mathematische Präzision von LiDAR mit dem Fotorealismus eines hochauflösenden Videos.


Hier sind die spannendsten, aktuellen Entwicklungen und Nachrichten (Stand Frühjahr 2026) zu genau diesem Thema:

1. Von 3D zu 4D: Splatting in Bewegung

Die neueste technische Grenze ist das sogenannte 4D Splatting – hier kommt die Zeit als vierte Dimension hinzu. Statt nur statische Räume einzufrieren, können mittlerweile ganze Bewegungsabläufe räumlich erfasst werden. Ein prominentes kommerzielles Beispiel aus der jüngsten Zeit ist das Musikvideo „Helicopter“ von A$AP Rocky. Dort wurden Performer mit 56 Kameras aufgenommen und das Footage in 4D-Splats umgewandelt, was völlig unmögliche Kamerafahrten und Perspektivenwechsel nachträglich im digitalen 3D-Raum ermöglichte.

2. Volumetrische 3D-Immobilien (Zillow SkyTour)

Im März 2026 hat das große Immobilienportal Zillow detaillierte Einblicke in seine neue KI-Engine SkyTour gegeben. Zillow nutzt Drohnen-Videos von Immobilien und wandelt diese mithilfe von 3D Gaussian Splatting komplett automatisch in interaktive, volumetrische 3D-Szenen um. Nutzer können so nicht nur virtuell durch ein Haus laufen, sondern das komplette Gebäude inklusive Bäumen und Umgebung von außen wie ein fotorealistisches Puppenhaus betrachten und stufenlos hineinzoomen.

3. Hollywood-Technik durch Smartphones

Auf der großen Branchenmesse NAB im April 2026 präsentierte das Unternehmen Radiant Images ein Rig aus 24 herkömmlichen iPhones. Statt wie beim klassischen „Bullet-Time“-Effekt (bekannt aus dem Film Matrix) die Frames zwischen den Kameras mühsam per Hand zu interpolieren, füttern sie die Videos in einen Gaussian Splatting Algorithmus. Das Ergebnis ist eine vollständig rekonstruierte 3D-Szene, durch die Regisseure im Nachhinein stufenlos fliegen, die Brennweite ändern und die Umgebung bearbeiten können.

4. Integration in Standard-Software

Die Technologie ist mittlerweile so weit gereift, dass sie die Forschungslabore verlassen hat und in die Standard-Software der Film- und Design-Industrie einzieht. So wurde 3DGS Anfang 2026 nativ in den mächtigen Industrie-Renderer V-Ray 7 integriert. 3D-Artists können nun reale Umgebungen, die sie mit dem Smartphone als Video gescannt haben, nahtlos mit computergenerierten Objekten kombinieren.

5. Das "Einfrieren" von Erinnerungen für Konsumenten

Nicht nur Profis nutzen die Technik. Magazine wie Lifehacker berichten aktuell vermehrt über Consumer-Apps (wie z. B. Splat Studio), die es jedem ermöglichen, aus simplen Handyvideos sogenannte „Dioramen“ zu erstellen. Der Trend geht dahin, dass Menschen Räume oder Momente – wie das Familienwohnzimmer an Weihnachten – als komplett begehbare 3D-Erinnerung auf dem Smartphone konservieren, anstatt nur flache Fotos zu schießen.

Radiant Images: 24 iPhones für Next-Gen Bullet Time durch Gaussian Splatting
https://www.youtube.com/watch?v=5MXc8A2gEcE

Dieses Video zeigt sehr anschaulich am Beispiel eines iPhone-Setups, wie aus synchronisierten Videoaufnahmen dank Gaussian Splatting eine völlig frei navigierbare 3D-Szene für virtuelle Kamerafahrten entsteht.