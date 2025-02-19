# Template literals


Template literals are strings that can contain expressions embedded in them.

They allow:

- Multi-line strings without `\n`.
- String interpolation.
- Embedded expressions.

## String interpolation: Injecting variables into strings

Before ES6, inserting variables into strings was done using the `+` operator.


### Before template literals


```js

const message = 'Hello'
const name = 'John'

console.log(message + ' ' + name)

```

### With template literals


```js

const message = 'Hello'
const name = 'John'

console.log(`${message} ${name}`);

```

## Multi-line strings

Multi-line strings required `\n` or joining with `+` operator.

```js

const multi-line= "Hello John \n" + "How are you?";

console.log(multi-line);

```


```js

const multi-line= `Hello John

How are you?`;

console.log(multi-line);

```

### Expressions inside template literals

Template literals can also contain expressions.

```js
let a =10
let b =20

console.log(`The sum of ${a} and ${b} is ${a+b}`);

```

