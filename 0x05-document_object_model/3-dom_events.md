# DOM Events

An event in the DOM is an action or occurrence that happens in the browser which the browser can respond to.

Events are triggered by user interactions such as clicks, key presses or mouse movements.


## Some popular DOM events

`onclick`
Triggered when the user clicks on an HTML element.

```js

const btn = document.getElementById("btn");
btn.onclick = function () {
  console.log("Button Clicked");
};


```

`onmouseover`

Triggered when the user hovers over an HTML element.

`onmouseout`

Triggered when the user moves the mouse out of an HTML element.

`onkeydown`

Triggered when the user presses a key on the keyboard.

Usually called on the **document**, i.e.,` document.onkeydown = function() {}`

`onkeyup`

Triggered when the user releases a key on the keyboard.

Usually called on the document, i.e., `document.onkeydown = function() {}`

`onload`

Triggered when the HTML document has finished loading.


Called on **window**, i.e., `window.onload = function() {}`

`onfocus`

Triggered when the user focuses on an HTML element.