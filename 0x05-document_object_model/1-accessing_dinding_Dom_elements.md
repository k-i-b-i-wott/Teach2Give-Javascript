# Accessing/Finding Dom Elements

To access any element in an HTML page, we first start by accessing the `document` object.

The document object is the owner of all other objects on the page.

## Methods for accessing DOM elements


`document.getElementById(elementId)`


Finds an element with id equivalent to `elementId`.

```hmtl
<button id="my-button">Click Me</button>
```

```JS
const button = document.getElementById("my-button");
console.log(button); // <button id="my-button">Click Me</button>
```

### `document.getElementsByTagName(name)`

Finds all the elements that match the tag name passed, e.g., finding all paragraph elements in a page.

It returns a NodeList of all elements that match the tag name passed.

You can index the specific element you want from this element the same way you would index an array.

```html
<p>Hello, World</p>
<p>JavaScript is awesome</p>
<p>JavaScript is great</p>

```

```js

const paragraphs = document.getElementsByTagName("p");
console.log(paragraphs); // [p, p, p]

```

### `document.getElementsByClassName(className)`

Finds and returns a NodeList of all HTML elements with class attribute similar to the class specified.

You can index the specific element you want from this element the same way you would index an array.

```html

<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>

```
```js
const texts = document.getElementsByClassName("text");
console.log(texts); // [p.text, p.text]

```

### `document.querySelector(selector)`

Finds the first element that matches the CSS selector passed.

```html

<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>

```

```js

const text = document.querySelector(".text");
console.log(text); // <p class="text">Hello, World</p>

```

### `document.querySelectorAll(selector)`

Finds all the elements that match the CSS selector passed.

```html

<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>

```

```js
const paragraphs = document.querySelectorAll('p');
console.log(paragraphs); // [p.text, p.text, p]

```