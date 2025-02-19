# Changing DOM Elements

We can change the **Content, styling** and **Attributes** of DOM elements.


## Changing the content of HTML elements

### `innerHTML`

The `innerHTML` property sets or returns the HTML content of an HTML element.

```html
<div id="my-div">
    <h1>Hello, world</h1>
    <p>JavaScript is awesome</p>
</div>

```

```js
const div = document.getElementById("my-div");
console.log(div.innerHTML);
div.innerHTML = `<h1>New content</h1>`;
console.log(div.innerHTML);

```

### `innerText`

The `innerText` property sets or returns the text content of an HTML element.

```html
<div id="my-div">
    <h1>Hello, world</h1>
    <p>JavaScript is awesome</p>
</div>

```

```js

const div = document.getElementById("my-div");
console.log(div.innerText);
div.innerText = "New content";
console.log(div.innerText);

```


### `textContent`

Sets or gets the text content of an element and its descendants without preserving the HTML tags.

It is more consistent across browsers compared to `innerText`.


## Changing the attribute of HTML elements

- We can use `element.attributes =value` to get all the attributes of an element.


``` html
<h1 class="title" id="title">Hello, world</h1>

```

```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.id = "awesome-title";
console.log(title); // <h1 class="title" id="awesome-title">Hello, world</h1>

```

- We can  also use `element.setAttribute(attributeName, Value)` to set the value of an attribute.

```html
<h1 class="title" id="title">Hello, world</h1>

```

```js

const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.setAttribute("id", "awesome-title");
console.log(title);

```

## Changing the styling of HTML elements

We can use the `element.style.property` object to change the styling of an element.


It is important to input the value in double quotes even if it is a number.

```js
const title = document.getElementById("title");
title.style.border = "3px solid red";
title.style.fontSize = "48px";
title.style.borderRadius = "5px";

```

### Changing styling in JavaScript using CSS classes

- `element.classList.add()`: adds one or more classes to an element.

- `element.classList.remove()`: removes one or more classes from an element.

- `element.classList.toggle()`: toggles the specified class, it is present, it is removed, if it is absent, it is added.

-  `element.classList.contains()`: checks if the 
specified class is present in the element.

- `element.classList.replace()`: replaces the specified class with another class.
- `element.style.setProperty()`: sets the value of a CSS property on an element.

