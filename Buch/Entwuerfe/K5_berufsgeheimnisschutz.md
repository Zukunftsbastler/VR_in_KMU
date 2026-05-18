# Entwurf: Berufsgeheimnisschutz und VR — Einschub Kap. 08

> **Zielstelle im Buch:** `Buch/08_technische_implementation.md`
> Einzufügen unter dem bestehenden Abschnitt „Rechtliche und ethische Aspekte" als neuer
> Unterpunkt **nach** dem DSGVO-Konformitätspunkt (derzeit Punkt 1).
> Alternativ: als eigenständiger Unterabschnitt `### Berufsgeheimnisschutz` direkt
> nach dem bestehenden Unterabschnitt „Rechtliche und ethische Aspekte".
>
> **Charakter:** Klarstellung und Einordnung — kein neues Rechtsgebiet, sondern
> Hinweis auf spezifische Besonderheit bei regulierten Berufsgruppen.
>
> **Framework-Verortung:** TI (Plattformwahl, Datenhaltung), EU (externer Einsatz)
> **Testfall-Relevanz:** F08 (Steuerberatung), F13 (Rechtsanwaltskanzlei), F18 (Zahnarztpraxis)

---

### Berufsgeheimnisschutz: Kein VR-spezifisches Problem — aber eine plattformspezifische Frage

Für Unternehmen und Freiberufler, die gesetzlichen Berufsgeheimnispflichten unterliegen, stellt sich bei der Einführung jedes neuen Kommunikationsmediums dieselbe Grundfrage: Kann dieses Medium für vertrauliche Mandats- oder Patientengespräche genutzt werden, ohne die Schweigepflicht zu verletzen?

Betroffen sind insbesondere:

- **Rechtsanwälte** (§ 43a BRAO i.V.m. § 203 StGB): Das Mandatsgeheimnis ist strafbewehrt.
- **Ärzte und Zahnärzte** (§ 203 StGB): Die ärztliche Schweigepflicht gilt für alle Patientendaten, unabhängig vom Übertragungsweg.
- **Steuerberater und Wirtschaftsprüfer** (§ 57 Abs. 1 StBerG, § 30 AO): Steuer- und Mandatsgeheimnis mit berufsrechtlichen Sanktionen bei Verstoß.

**VR als Technologiekategorie schafft hier keine neue Rechtslage.** Rechtsanwälte führen seit Jahren Mandantengespräche per Telefon, verschlüsselter E-Mail und Videokonferenz — alles über Infrastruktur, die nicht unter ihrer unmittelbaren Kontrolle steht. Die maßgebliche Frage ist nicht, ob ein Dritter theoretischen Zugriff auf Übertragungswege hat, sondern ob **verhältnismäßige technische und organisatorische Schutzmaßnahmen** getroffen wurden und ob der Plattformbetreiber ein legitimes Interesse an den übertragenen Inhalten hat.

#### Der entscheidende Unterschied: Neutraler Infrastrukturanbieter vs. datenverwertende Plattform

Ein Telekommunikationsanbieter oder ein Enterprise-Videokonferenzdienst bietet Übertragungsinfrastruktur an, ohne ein eigenes wirtschaftliches Interesse an den Gesprächsinhalten zu haben. Meta Platforms Inc. hingegen betreibt ein Geschäftsmodell, das auf der Auswertung von Nutzungsverhalten, biometrischen Daten (Augenbewegungen, Handgesten, Raumerfassung) und Interaktionsmustern basiert. Dieser Unterschied ist für regulierte Berufsgruppen rechtlich relevant — nicht VR als solches, sondern **die spezifische Plattform und ihr Geschäftsmodell**.

Praktisch bedeutet das: Für Berufsgeheimnisträger ist die Nutzung von Meta Quest in sensiblen Gesprächskontexten aus denselben Gründen problematisch wie die Nutzung eines kostenlosen E-Mail-Dienstleisters, dessen Geschäftsmodell auf Inhaltsauswertung basiert — unabhängig davon, ob alle DSGVO-Formalitäten erfüllt sind.

#### Handlungsempfehlung

Die Lösung liegt in der **Plattformwahl**, nicht in einem Verzicht auf VR:

| Plattformtyp | Eignung für regulierte Berufe | Begründung |
|---|---|---|
| Meta Quest (Horizon Workrooms) | Nicht empfohlen | Biometrische Daten gehen an Meta; Geschäftsmodell basiert auf Datenverwertung |
| Microsoft Teams Mesh (Azure-hosted) | Prüfbar | Enterprise-AVV möglich; keine Datenmonetarisierung; Microsoft-Zertifizierungen (ISO 27001, SOC 2) |
| HTC Vive Focus + lokale Plattform | Geeignet | Keine Cloud-Pflicht; Datenhaltung lokal möglich |
| Varjo (EU-Hersteller) + eigener Server | Gut geeignet | EU-Datenhaltung, keine werbebasierte Monetarisierung |
| WebXR mit selbst gehostetem Server | Gut geeignet | Vollständige Datenkontrolle; kein Headset-Konto erforderlich |

> **Hinweis für die Praxis:** Die Einschätzung, ob eine konkrete VR-Plattform mit der jeweiligen Berufsgeheimnispflicht vereinbar ist, sollte im Zweifelsfall mit der zuständigen Berufsorganisation (z. B. Rechtsanwaltskammer, Ärztekammer) oder dem zuständigen Datenschutzbeauftragten abgestimmt werden. Für Unternehmen in Schleswig-Holstein steht das **Unabhängige Landeszentrum für Datenschutz (ULD SH)** als kostenlose Anlaufstelle für Vorabanfragen zur Verfügung.
