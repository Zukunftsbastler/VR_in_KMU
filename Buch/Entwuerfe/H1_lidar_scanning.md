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

Als Hardware diente ein **iPhone 15 Pro** mit dem integrierten LIDAR-Scanner; als Software wurde die **3D Scanner App** (Apple App Store) eingesetzt, die für Endanwender eine einfache Point-and-Shoot-Erfahrung verspricht.

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
