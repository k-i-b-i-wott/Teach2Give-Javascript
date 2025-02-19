# Arrow functions
Arrow functions (`=>`) were introduced to provide more concise syntax for writing functions in Javascript

```js
Before
function add(a, b) {
    return a + b;
}
console.log(add(4,12));

```
```js

After

const add= (a,b)=>a+b;

console.log(add(4,12));

```

Arrow functions can only be used object methods

Arrow functions excel in scenarios such as **call back for array methods, events listeners, and situations where we want to simplify our (function)**