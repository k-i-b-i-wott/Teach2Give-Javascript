# ES6 Modules

ES6 introduced the concept of modules, which allow you to encapsulate code into self-contained units called modules.

Modules provide a way to organize and reuse code, making it easier to maintain and reuse code across different parts of your application.

## Important Note About ES6 Modules

If you are using ES6 Modules in a browser, you need to add `type="module"` in the `<script>`

```js

<script type="module" src="script.js"></script>

```

To use ES6 Modules in a Node.js environment, you need to use the `import` keyword.

- Add `"type": "module"` to your `package.json` file.
- Use `.mjs` extension for your files


## Exporting and Importing in ES6 Modules

In ES6, you can export code from a module using either **named exports** or **default exports**

#### Named Exports

You can export multiple values from a module using the `export` keyword.

**File: mathUtils.mjs**

```js
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}

export function multiply(a, b) {
  return a * b;
}

```

You can then import them using the `import` keyword.

**File: main.mjs**

```js

import { add, subtract, multiply } from "./mathUtils.mjs";

console.log(add(2, 3)); // Output: 5
console.log(subtract(5, 2)); // Output: 3
console.log(multiply(3, 4)); // Output: 12

```
**Note: you must precede the file name with `./` when importing it.**

#### Using aliases for imports

You can rename imports using the `as` keyword.

```js
import { add as sum, subtract as difference, multiply } from "./mathUtils.mjs";
console.log(sum(5, 4));
console.log(difference(5, 4));
console.log(multiply(5, 4));

```
#### Import everything from a module

You can import everything from a module using the `*` keyword.

```js
import * as MathUtils from "./mathUtils.mjs";
console.log(MathUtils.add(5, 4));
console.log(MathUtils.subtract(5, 4));
console.log(MathUtils.multiply(5, 4));

```
### Default Exports

You can also export a default value from a module using the `export default` keyword.

**File|:logger.mjs**

```js

export default function log(message) {
  console.log(`Log: ${message}`);
}

```

Default exports don't need to be wrapped in curly braces`{}`.

You can import a default export using the `import` keyword.

**File: main.mjs**

```js

import log from "./logger.mjs";

log("Hello, world!");

```