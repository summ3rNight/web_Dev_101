# HyperText Markup Language

## Is HTML Enough for a Website?

- HTML alone can create simple pages. Modern websites also need:
  - CSS (for style/design)
  - JavaScript (for interactivity)

## Basic

**creating structure content on web pages, define element like: paragraph, headings, links, images, ...**

- moste element:

```html
<p>Hello</p>
```

- void element: does not have open and close tag(<>)

```html
<img />
```

---

## Attributes

**HTML elements can have attributes that change their behavior**

- An attribute is extra information added inside the opening tag of an HTML element.
- It customizes the behavior or appearance of the element.

```html
<element attribute="value"></element>
<img src="img-url" alt="image description" />
```

- Common Attributes

```html
<a href="https://www.example.com">Visit</a>
<img src="img-url" alt="image description" />
```

- Boolean Attributes
  - Do not need a value. Presence alone activates them.

```html
<input type="checkbox" checked />
```

{checked makes the checkbox selected by default}

- other boolean attributes:
  - disabled – makes an element inactive
  - readonly – makes form input non-editable
  - required – makes form input mandatory

---

## Role of the Link Element in HTML, and How Can It Be Used to Link to External Stylesheets?

**link - element connects your HTML document to external resources like:** - CSS stylesheets, Fonts, Icons (e.g., favicons)

```html
<link rel="stylesheet" href="./styles.css" />
```

{rel: defines the relationship to the HTML document → stylesheet for CSS | href: location of the file (e.g., ./styles.css)}

- example 1: linking a css file

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Examples of the link element</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```

- example 2: linking google fonts

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap"
  rel="stylesheet"
/>
```

{preconnect: speeds up loading by opening early connections | Google Fonts are free and customizable}

- example 3: linking a favicon

```html
<link rel="icon" href="favicon.ico" />
```

{A favicon is a small icon shown in left of a browser tab | It's used for branding}

---

## What Is an HTML Boilerplate, and Why Is It Important?

**A boilerplate is a ready-made HTML template, It provides the basic structure every web page needs**
_Think of it as the foundation of a house—it saves time and ensures correct setup._

- example 1: Basic HTML Boilerplate Example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>freeCodeCamp</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    <!-- Your visible content goes here -->
  </body>
</html>
```

1. `<!DOCTYPE html>` : Declares the HTML version (HTML5), Helps browsers render the page correctly.
2. `<html lang="en">` : Root element of the page, the lang attribute specifies the language of the content.
3. `<head> section` : Contains metadata and non-visible content.
4. `<body> section` : Contains the visible content of the webpage

**Why Use a Boilerplate?**
_Ensures cross-browser compatibility.
Follows best practices.
Saves setup time for each new project.
Can be customized as you gain experience._

- **Where would you set the character encoding for your page?**
  _a meta element in the head_
- **Where would you set the language for your page?**
  _in the opening html tag_
- **What purpose does a boilerplate serve?**
  _Provides a starting structure for your websites, Ensures you are not missing any essential elements,
  Allows you to get started writing the content of your page faster._

---

## What Is UTF-8 Character Encoding, and Why Is It Needed?

**It is a character encoding that tells computers how to store and display text,
Every letter, number, and symbol is stored as one or more bytes (1 byte = 8 bits).**

- How to Use It in HTML : You include UTF-8 with a meta tag in the <head> section

```html
<meta charset="UTF-8" />

<! example !>
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Examples of the UTF-8 encoding</title>
  </head>
  <body>
    <p>Café</p>
    <!-- "é" displays correctly because of UTF-8 -->
  </body>
</html>
```

_Best Practice: Always include <meta charset="UTF-8" /> in your HTML documents,
It ensures correct rendering of multilingual text and special characters._

- **Which attribute is used to set the UTF-8 character encoding for HTML documents?**
  _charset_
- **What is character encoding?**
  _a methode cpomputers use to store char as data_
- **How many bits are inside a byte?**
  _8_

---

## What are Div Elements and When Should You Use Them?

**`<div>` steht für "Content Division" und ist ein nicht-semantisches Container-Element, Es dient dazu, andere HTML-Elemente zu gruppieren (z. B. Überschriften, Absätze, Bilder).**

```html
<div>
  <h1>I am a heading</h1>
  <p>I am a paragraph</p>
</div>
```

_Die `<h1>` und `<p>` befinden sich gemeinsam im Container `<div>`_

### `<div>` vs. `<section>`

- `<div>` hat keine semantische Bedeutung (der Browser weiß nicht, was der Inhalt ist).

- `<section>` ist ein semantisches Element – es sagt dem Browser, dass es sich um einen eigenen Abschnitt handelt.

_Faustregel:
Verwende `<div>` für neutrale Gruppierungen, und `<section>`, `<article>`, `<nav>` usw. für bedeutungsvolle Strukturen._

**What semantic meaning does a div element have?**
_The div element has no semantic meaning._

**Which of the following is the correct syntax for a div element?**
_`<div>`content goes here`</div>`_

**Which of the following HTML elements is commonly used to group content into distinct sections?**
_section_

---

## What Are IDs and Classes, and When Should You Use Them?

**id ist ein eindeutiger Bezeichner für ein einzelnes HTML-Element.**

```html
<h1 id="title">Movie Review Page</h1>
```

In CSS greifst du mit # auf eine id zu:

```css
#title {
  color: red;
}
```

_wichtig:
Eine id darf nur einmal pro Seite vorkommen._

```html
<!-- Falsch: -->
<h1 id="main heading">...</h1>

<!-- Richtig: -->
<h1 id="main-heading">...</h1>
```

### Was ist class?

**class wird verwendet, um mehrere Elemente mit denselben Eigenschaften zu versehen.**

```html
<div class="box"></div>
<!-- Mehrere Klassen sind mit Leerzeichen trennbar -->
<div class="box red-box"></div>
```

In CSS greifst du mit . auf eine Klasse zu:

```css
.box {
  width: 200px;
  height: 200px;
  border: 2px solid black;
}
```

### Wann verwende ich id und wann class?

| Merkmal         | id                                   | class                             |
| --------------- | ------------------------------------ | --------------------------------- |
| Einzigartigkeit | Muss einzigartig sein                | Kann mehrfach verwendet werden    |
| CSS-Syntax      | #idname                              | .classname                        |
| Anwendung       | Für ein bestimmtes Element           | Für mehrere gleichartige Elemente |
| Beispiel        | Navigation, ein bestimmter Abschnitt | Boxen, Buttons, Layout-Gruppen    |

**When should you use an id versus a class?**
_Use an id when you need a unique identifier for a specific element, and use a class when you want to apply styles or behavior to multiple elements_

**What happens if you use the same id more than once in your HTML?**
_It can lead to unwanted results and issues when trying to apply styles or targeting an element in JavaScript._

**Which of the following is NOT a correct value for the id attribute?**
_id="main heading"_

---

## Was sind HTML Entities?

**HTML-Entities sind Sonderzeichen-Codes, die verwendet werden, um reservierte Zeichen oder Sonderzeichen korrekt in HTML darzustellen.**

**Sie werden genutzt, wenn ein Zeichen normalerweise vom Browser als HTML interpretiert wird, z. B. <, > oder &.**

- Beispielproblem

```html
<p>This is an <img /> element</p>
```

_problem:
Der Text zeigt nur: This is an element, `<img />` wird vom Browser als echtes HTML-Element interpretiert._

- Lösung mit Entities

```html
<p>This is an &lt;img /&gt; element</p>
```

_`&lt;` steht für <, `&gt;` steht für >
Ausgabe im Browser: This is an `<img />` element_

### Arten von HTML Entities

| Typ                       | Beispiel | Beschreibung                                       |
| ------------------------- | -------- | -------------------------------------------------- |
| **Named Reference**       | `&lt;`   | Name zwischen `&` und `;`, z. B. `&copy;`, `&amp;` |
| **Decimal Reference**     | `&#60;`  | Dezimalwert des Zeichens                           |
| **Hexadecimal Reference** | `&#x3C;` | Hexadezimalwert mit `x`, z. B. `&#xA9;` für ©      |

### Häufige HTML Entities

| Zeichen | Entity    | Beschreibung                |
| ------- | --------- | --------------------------- |
| `<`     | `&lt;`    | Kleiner-als-Zeichen         |
| `>`     | `&gt;`    | Größer-als-Zeichen          |
| `&`     | `&amp;`   | Und-Zeichen                 |
| `"`     | `&quot;`  | Anführungszeichen           |
| `'`     | `&apos;`  | Einfaches Anführungszeichen |
| `©`     | `&copy;`  | Copyright-Zeichen           |
| `™`     | `&trade;` | Trademark-Zeichen           |

- **Verwende HTML Entities, wenn du Sonderzeichen anzeigen willst, die sonst vom Browser als HTML interpretiert würden.**

- **Besonders nützlich beim Anzeigen von Code, Symbolen oder typografischen Zeichen.**

**What is an HTML entity (character reference)?**
_A set of characters used to represent a reserved character in HTML._

**What are the three types of character references?**
_Named, Decimal numeric, and Hexadecimal numeric character references._

**Which of the following is the correct syntax for a named character reference?**
_`&amp;`_

---

## Was ist das `<script>`-Element?

**Das `<script>`-Element wird verwendet, um ausführbaren Code (meist JavaScript) in HTML-Seiten einzubinden.**

**JavaScript macht Webseiten interaktiv (z. B. Spiele, Formulare, Bild-Slider).**

- Beispiel: Inline-JavaScript

```html
<body>
  <script>
    alert("Welcome to freeCodeCamp");
  </script>
</body>

<!--Führt beim Laden der Seite ein Pop-up (alert) aus. Der Code steht direkt innerhalb der HTML-Datei. -->
```

## Externer JavaScript-Code

_Best Practice: JavaScript in externe Dateien auslagern_

```html
<script src="pfad-zur-datei.js"></script>
<!--src steht für source (Quelle) – dort gibst du den Pfad zur .js-Datei an-->
```

## Warum externe Dateien?

**Separation of Concerns (Trennung von Verantwortlichkeiten):**

1. HTML = Struktur
2. CSS = Design
3. JavaScript = Verhalten / Interaktivität

**→ So bleibt dein Code übersichtlich, wartbar und wiederverwendbar.**

### fazit

- Verwende `<script>` für JavaScript-Code
- Nutze externe Dateien, um HTML und JS zu trennen
- Verwende src="...", um externe JS-Dateien einzubinden

---

## Was ist SEO?

**SEO (Suchmaschinenoptimierung) ist die Praxis, Webseiten so zu gestalten, dass sie in Suchmaschinen besser sichtbar und höher platziert sind.**

### Was ist die meta description?

**Eine meta-Beschreibung ist eine kurze Zusammenfassung des Inhalts deiner Webseite.**

**Sie wird nicht auf der Seite angezeigt, sondern von Suchmaschinen verwendet.**

- Beispiel:

```html
<meta
  name="description"
  content="Discover expert tips and techniques for gardening in small spaces, choosing the right plants, and maintaining a thriving garden."
/>
```

### Wo erscheint die Beschreibung?

**In den Suchergebnissen (Snippets) – also direkt unter dem Link zur Website bei Google & Co.**

- Beispiel:

```makefile
r/FreeCodeCamp: Dies ist das offizielle Subreddit der freeCodeCamp.org-Community...
```

### Best Practices

- Kurz & präzise formulieren (max. ca. 160 Zeichen)
- Klarer Nutzen oder Inhalt der Seite vermitteln
- Relevante Schlüsselwörter einbauen (aber kein Keyword-Spamming)
- Ziel: Nutzer zum Klicken motivieren

### Einfluss auf SEO

- Die meta description verbessert nicht direkt das Ranking, aber:
  - Sie beeinflusst die Klickrate (CTR) – und damit indirekt den Erfolg deiner Seite.
  - Bessere CTR = mehr Besucher = besseres Ranking möglich

**Which element is used to set the description for a web page?**
_meta_

**What does SEO stand for?**
_search engine optimization_

**Where does the page's description typically show up?**
_In the search engine results page._

### Fazit

- Verwende das meta description-Element für klare, ansprechende Seitenbeschreibungen
- Nicht sichtbar, aber wichtig für Suchmaschinen und Nutzer
- Teil einer guten SEO-Strategie

---

## Was sind Open Graph Tags?

**Open Graph Tags (OG-Tags) sind spezielle `<meta>`-Elemente im `<head>` einer HTML-Seite.**

**Sie bestimmen, wie deine Webseite beim Teilen in sozialen Medien angezeigt wird (z. B. auf Facebook, LinkedIn, Twitter).**

**Sie helfen, ansprechende Vorschauen mit Titel, Bild, Beschreibung usw. zu erstellen.**

### Wichtige OG-Tags:

| OG-Tag     | Zweck                                                            |
| ---------- | ---------------------------------------------------------------- |
| `og:title` | Titel, der im Beitrag auf Social Media angezeigt wird            |
| `og:type`  | Art des Inhalts (z. B. `website`, `article`, `video`)            |
| `og:image` | Bild-Vorschau (sollte groß & hochwertig sein, z. B. 1200×630 px) |
| `og:url`   | URL zur Originalseite (hilft bei Tracking & Klarheit)            |

```html
<meta content="freeCodeCamp.org" property="og:title" />
<meta property="og:type" content="website" />
<meta
  content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
  property="og:image"
/>
<meta property="og:url" content="https://www.freecodecamp.org" />
```

### Einfluss auf SEO

- OG-Tags wirken sich nicht direkt auf das Google-Ranking aus, aber:
  - Sie verbessern das Erscheinungsbild in Social-Media-Feeds.
  - Das kann zu mehr Klicks (CTR) führen.
  - Eine höhere CTR kann Suchmaschinen signalisieren, dass die Seite relevant und interessant ist.

**What are open graph properties used for?**
_To set how your website's content will be seen on different social media platforms._

**What does the property="og:title" do in the meta element?**
_It specifies the title of your web page content when it is shared on social media platforms._

**What does the property="og:type" do in the meta element?**
_It specifies the type of content used for your web page when it is shared on social media platforms._

---

## Audio and Video Elements

```html
<audio src="CrystalizeThatInnerChild.mp3" control></audio>
<!-- -- The audio element with control to enable in page-->

<audio
  src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3"
  loop
  controls
></audio>
<!-- loop to restart audio-->

<audio
  src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3"
  loop
  controls
  muted
></audio>
<!-- muted when browser start-->

<audio controls>
  <source src="audio.ogg" type="audio/ogg" />
  <source src="audio.wav" type="audio/wav" />
  <source src="audio.mp3" type="audio/mpeg" />
</audio>
<!-- browser start with ogg type, if cant play audio then switch to wav ... -->

<video
  src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
  loop
  controls
  muted
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
  width="620"
></video>
<!--poster is for show a img while video load, fix width format-->
```
