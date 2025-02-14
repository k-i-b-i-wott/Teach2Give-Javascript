# Type Coercion and Type Conversion


In JavaScript, both type **coercion** and type **conversion** involve changing a value from one data type to another, but they differ in how they happen.

# Type Coercion (Implicit Conversion)

Happens automatically when JavaScript tries to perform operations between different data types.

Common in comparisons` (==)`, string concatenation `(+)`, and arithmetic operations.

Type coercion sometimes leads to unexpected results.

**Examples:**


```js

console.log(5 + "5"); // "55" (Number coerced into a string)
console.log("5" - 2); // 3 (String coerced into a number)
console.log(true + 1); // 2 (true coerced into 1)
console.log(false + "10"); // "false10" (false coerced into string)

```


# Type Conversion (Explicit Conversion)

Happens when you manually convert the data type of a value

## Methods of Explicit Conversion

<ul>
    <li>Convert to string using `String()` or `toString()`.</li>
</ul>

```js

console.log(String(382));
console.log((382).toString());

```


<ul>
    <li>Convert to number `using Number()`, `parseInt()` or `parseFloat()`</li>
</ul>

```js

console.log(Number("382"));
console.log(parseInt("382"));
console.log(parseFloat("382"));
console.log(parseInt("42px"));


```

<ul>
    <li>Convert to boolean using `Boolean()`</li>
</ul>

**. Falsy values:** 0, "", null, undefined, NaN, false.  
**. Truthy values:**  everything else</li>


```js

console.log(Boolean(0)); // false
console.log(Boolean("hello")); // true
console.log(Boolean(null)); // false


```




