# DOM Event Listener Methods

The `addEventListener()` method attaches an event handler to a specified element.

It attaches an event handler without overwriting existing handlers.

It takes in three parameters (for now let's focus on the first two).

The first parameter is the type of event passed in as a string e.g.,**click, mousedown, mouseenter** e.t.c.

The second parameter is the function we want to call when the specified event occurs.

**Example:**


```js

const btn = document.getElementById("btn");

btn.addEventListener("click", function () {
  console.log("Button Clicked");
});

```