# HyperText Markup Language
## Basic
- creating structure content on web pages, define element like: paragraph, headings, links, images, ...
- moste element:
```html
<p>Hello</p>
```
- void element: does not have open and close tag(<>)
```html
<img>
```
## Attributes
- HTML elements can have attributes that change their behavior.
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
checked makes the checkbox selected by default.
- other boolean attributes:
    - disabled – makes an element inactive
    - readonly – makes form input non-editable
    - required – makes form input mandatory


## Is HTML Enough for a Website?
- HTML alone can create simple pages. Modern websites also need:
    - CSS (for style/design)
    - JavaScript (for interactivity)


