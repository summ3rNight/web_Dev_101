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
<img>
```
---

## Attributes
**HTML elements can have attributes that change their behavior**
- An attribute is extra information added inside the opening tag of an HTML element.
- It customizes the behavior or appearance of the element.
```html
<element attribute="value"></element>
<img src="img-url" alt="image description">
```
- Common Attributes
```html
<a href="https://www.example.com">Visit</a>
<img src="img-url" alt="image description">
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
**link - element connects your HTML document to external resources like:**
    - CSS stylesheets, Fonts, Icons (e.g., favicons)

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
<link href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap" rel="stylesheet"/>
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
*Think of it as the foundation of a house—it saves time and ensures correct setup.*

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
*Ensures cross-browser compatibility.
Follows best practices.
Saves setup time for each new project.
Can be customized as you gain experience.*

- **Where would you set the character encoding for your page?**
*a meta element in the head*
- **Where would you set the language for your page?**
*in the opening html tag*
- **What purpose does a boilerplate serve?**
*Provides a starting structure for your websites, Ensures you are not missing any essential elements, 
Allows you to get started writing the content of your page faster.*
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
<p>Café</p>  <!-- "é" displays correctly because of UTF-8 -->
</body>
</html>
```

*Best Practice: Always include <meta charset="UTF-8" /> in your HTML documents,
It ensures correct rendering of multilingual text and special characters.*

- **Which attribute is used to set the UTF-8 character encoding for HTML documents?**
*charset*
- **What is character encoding?**
*a methode cpomputers use to store char as data*
- **How many bits are inside a byte?**
*8*
---




