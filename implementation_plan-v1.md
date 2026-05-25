# Umsetzungskonzept: Kulturkommission Hettlingen Webauftritt

Dieses Konzept beschreibt den Aufbau, das Design und die Struktur für den neuen Webauftritt der Kulturkommission Hettlingen. Die Website wird modern, ansprechend und voll funktionsfähig gestaltet. Sie basiert auf reinem HTML5 und modernem Vanilla CSS, um eine hervorragende Ladezeit, hohe Responsivität und visuelle Eleganz zu gewährleisten.

## Designkonzept & visuelle Ästhetik

Um den Anforderungen an ein elegantes, unaufdringliches Design mit hellen Pastellfarben und transparenten Containern gerecht zu werden, implementieren wir ein durchdachtes Design-System:

- **Farben**: Ein harmonisches, pastellfarbenes Farbschema mit weichen Verläufen:
  - Primär/Hintergrund-Akzente: Soft Lavender (`#f0ecfc`) und Blassrosa (`#fff5f5`)
  - Sekundär-Akzente: Salbeigrün (`#e6f4ea`) und Sand/Creme (`#fdfbf7`)
  - Textfarbe: Dunkles Anthrazit (`#2d3748`) für hervorragende Lesbarkeit und Barrierefreiheit
  - Akzente/Interaktion: Zartes Roségold und Flieder mit sanften Übergängen
- **Transparenz & Glassmorphismus**: Die Inhalts-Container werden mit einer 20%igen Transparenz gestaltet (80% Opazität: `rgba(255, 255, 255, 0.8)`). Ein zusätzlicher weicher Unschärfe-Filter (`backdrop-filter: blur(12px)`) und eine dezente weiße Kontur verleihen den Containern einen hochwertigen, modernen "Glass"-Look, durch den die Hintergrundbilder elegant durchschimmern.
- **Typografie**: Wir nutzen die moderne, gut lesbare Schriftart **Outfit** oder **Inter** von Google Fonts.
- **Interaktivität**:
  - Weiche Hover-Effekte mit Mikromotionen bei Buttons, Links und Tabellenzeilen.
  - Bild-Hover-Effekte mit leichtem Zoom und Schatten.
- **Responsivität**: Flexbox und CSS-Grid sorgen dafür, dass die Website auf allen Geräten (Desktop, Tablet, Smartphone) perfekt aussieht.

---

## Vorgesehene Seiten und Struktur

### 1. Startseite (`index.html`)

- **Hintergrund**: `Bilder/Zelglitrotte2.jpeg`
- **Header**:
  - Ein zweispaltiges, responsives Layout.
  - Linke Spalte: Container mit dem Titel **"Kulturkommission Hettlingen"** und dem beschreibenden Einleitungstext.
  - Rechte Spalte: Das offizielle Logo `Bilder/LogoKulturHettlingen.png`, harmonisch eingepasst auf die exakt gleiche Höhe wie der Text-Container.
- **Navigation**: Eine elegante, dezente Navigationsleiste mit den Links zu **Startseite**, **Organisation** und **Galerie**.
- **Agenda**:
  - Ein responsiver Container mit der Überschrift "Agenda".
  - Eine moderne, übersichtliche Tabelle mit den Spalten **Datum**, **Veranstaltung** (verlinkt auf die jeweilige Detailseite), **Ort** und **Vorschau** (mit dem entsprechenden Thumbnail-Bild als kleine, abgerundete Vorschau).
  - Einträge:
    1. 28.5.2026 | Theaterworkshop für Erwachsene | Singsaal der Primarschule Hettlingen | `Bilder/Theater-WS1.PNG` -> verlinkt auf `veranstaltung-001.html`
    2. 5.9.2026 | Theater Kanton Zürich "Der Menschenfeind" - Freilichttheater | Schulhaus Halden | `Bilder/Menschenfeind1.PNG` -> verlinkt auf `veranstaltung-002.html`
    3. 13.9.2026 | Constanze Constanze | Zelglitrotte | `Bilder/Constanze1.PNG` -> verlinkt auf `veranstaltung-003.html`
    4. 28.10.2026 | Figurentheater Shirai - "Kalif Storch" | Zelglitrotte | `Bilder/KalifStorch1.PNG` -> verlinkt auf `veranstaltung-004.html`
    5. 29.1.2026 | A Capella Ensemble Pagare mit "Best of best of" | Zelglitrotte | `Bilder/Pagare1.jpg` -> verlinkt auf `veranstaltung-005.html`

### 2. Organisation (`organisation.html`)

- **Hintergrund**: `Bilder/Sitzungszimmer.PNG`
- **Header & Navigation**: Struktur und Links analog zur Startseite, Titel **"Organisation"**.
- **Vereins-Info**:
  - Container mit dem Text zur Mitgliedschaft beim Verein **Pro Kultur Kanton Zürich** mit aktivem Link zu `https://prokultur-zuerich.ch/`.
- **Zuständigkeiten**:
  - Eine formschöne Tabelle mit den Spalten **Bereich**, **Zuständig** und **E-Mail** (E-Mail-Adressen als klickbare `mailto:`-Links gestaltet).
  - Strukturierte Darstellung aller Kommissionsmitglieder laut Spezifikation.

### 3. Galerie (`galerie.html`)

- **Hintergrund**: `Bilder/Zelglitrotte1.jpeg` (erzeugt einen stimmigen Bezug zur Location)
- **Titel**: **"Galerie"**
- **Navigation**: Strukturierte Links analog zu den anderen Seiten.
- **Inhalt**:
  - Strukturierte Zeilen für vergangene Veranstaltungen (z. B. das A Capella Konzert vom 29.1.2026 sowie weitere repräsentative Events).
  - Jede Zeile enthält das Datum und den Veranstaltungsnamen.
  - Direkt darunter befindet sich ein gestalteter Container mit 3 Bildern, die präzise auf eine Höhe von ca. 2.5 cm (ca. 95px bis 100px) skaliert sind.
  - Eingesetzte Bilder: Kombinationen aus `ZelglitrotteInnen.jpeg`, `ZelglitrotteInnen1.jpeg`, `ZelglitrotteInnen2.jpeg`, `Zelglitrotte.jpg` etc., um einen lebendigen Eindruck zu vermitteln. Ein Klick auf die Bilder öffnet eine elegante Vollbild-Vorschau (Lightbox-Effekt mittels purem CSS/JS).

### 4. Detailseiten der Veranstaltungen (`veranstaltung-nnn.html`)

Wir erstellen fünf individuelle Seiten für die in der Agenda gelisteten Veranstaltungen:
- **`veranstaltung-001.html`**: Theaterworkshop für Erwachsene (28.05.2026)
- **`veranstaltung-002.html`**: Theater Kanton Zürich "Der Menschenfeind" - Freilichttheater (05.09.2026)
- **`veranstaltung-003.html`**: Constanze Constanze (13.09.2026)
- **`veranstaltung-004.html`**: Figurentheater Shirai - "Kalif Storch" (28.10.2026)
- **`veranstaltung-005.html`**: A Capella Ensemble Pagare mit "Best of best of" (29.01.2026)

**Gemeinsames Layout der Detailseiten**:
- **Hintergrund**: Passende Bilder (z. B. `Bilder/ZelglitrotteInnen1.jpeg` oder eine leicht abgedunkelte Version des Eventbildes).
- **Inhalt-Container (20% transparent, Glass-Look)**:
  - Titel der Veranstaltung (groß und elegant)
  - Key-Metadaten in einer kompakten Info-Box: **Datum**, **Ort**
  - **Kontakt**: Name der zuständigen Person mit E-Mail-Link (Verknüpfung mit den Zuständigkeiten der Organisation, z. B. Lilly Zingg für Kindertheater, Valeria Enz-Dudas für Musik/Theater, Marco Recconico für Workshops).
  - Ein großer, ansprechender Bildbereich, der das Hauptbild der Veranstaltung (`Bilder/Theater-WS.PNG`, `Bilder/Menschenfeind.PNG`, `Bilder/Constanze.PNG`, `Bilder/KalifStorch.PNG` oder `Bilder/Pagare.jpg`) in hoher Qualität zeigt.
  - Ein liebevoll verfasster, detaillierter **Beschreibungstext** zur Veranstaltung.
  - Ein "Zurück zur Agenda"-Button mit geschmeidiger Animation.

---

## Technische Details & Dateistruktur

```
Kulturkommission/
├── index.html                  # Startseite mit Agenda
├── organisation.html           # Organisationsstruktur & Kontakte
├── galerie.html                # Bildergallerie vergangener Events
├── veranstaltung-001.html      # Detailseite: Theaterworkshop
├── veranstaltung-002.html      # Detailseite: Der Menschenfeind
├── veranstaltung-003.html      # Detailseite: Constanze Constanze
├── veranstaltung-004.html      # Detailseite: Kalif Storch
├── veranstaltung-005.html      # Detailseite: A Capella Pagare
├── style.css                   # Globales Design-System & Layout-Regeln
└── Bilder/                     # Ordner mit allen Bildressourcen (existiert bereits)
```

### Globale CSS-Datei (`style.css`)
Wir bündeln alle Design-Entscheidungen in einer gemeinsamen CSS-Datei, um Konsistenz zu garantieren.
- CSS Custom Variables für das Pastell-Farbschema.
- Globaler Reset und Typografie-Regeln (Import der Google Font 'Outfit').
- Styling der transparenten Container (`backdrop-filter`, `background: rgba(255, 255, 255, 0.8)`).
- Responsive Grids für Header, Navigation und Tabellen.
- CSS-Klassen für Tabellen, Buttons und Bildergalerien mit flüssigen Übergängen (`transition: all 0.3s ease`).

---

## Verifikationsplan

### 1. Visuelle Begutachtung
- Überprüfung der Transparenz der Container auf allen Seiten über verschiedene Hintergrundbilder hinweg.
- Prüfung der Bildplatzierung des Logos auf der Startseite (Höhe identisch zum Textcontainer).
- Überprüfung der Bildhöhen in der Galerie (2.5 cm / ca. 95px).

### 2. Funktionale Tests
- Verifizierung aller Links: Navigation zwischen den Hauptseiten, Links von der Agenda-Tabelle zu den jeweiligen Veranstaltungs-Detailseiten, "Zurück"-Buttons.
- Test der externen Links (Pro Kultur Kanton Zürich) und Mailto-Links in den Tabellen und Detailseiten.

### 3. Responsivitäts-Test
- Überprüfung auf mobilen Geräten und verschiedenen Bildschirmbreiten (Grid-Wrap-Effekte, Skalierung der Tabellen und Bilder).
