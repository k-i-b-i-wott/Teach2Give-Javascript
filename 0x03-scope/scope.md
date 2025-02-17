# Scope

**Scope** in Javascript dtermines the accessibility of variables.

It determines where a variable can be accessed.

There are two types of scope in JavaScript:

- Global Scope
- Function Scope(local scope)
- Block Scope(introduced in ES6)
- Lexical Scope

## Global Scope

A variable declared outside any function or block is considered globally scoped.

It is accessible anywhere in the JavaScript program.

```js

let x = 10;

function myFunction() {
    console.log(x); // accessible insiide the function

}

myFunction();

console.log(x); // accessible outside the function  

```

## Function Scope

Variables declared inside a function are only accessible within that function.
They cannot be accessd outside the function.

```js

function myFunction() {
    
    let x = 10;

    console.log(x); // accessible inside the function
}
console.log(x); // not accessible outside the function

```

## Block Scope( `let` and `const`)

Before ES6, JavaScript only had global scope and function scope. The var keyword did not support block scope.

However, ES6 introduced `let` and `const`, which have block scope.

A block is any code inside curly brackets `{}` (e.g., in `if`, `for`, `while` statements).

```js
if (true) {
  let age = 25;
  console.log(age); // works inside the block
}
console.log(age); // age is not defined
```


Variables declared with `let `and `const` are only accessible inside the block they are declared in.

`Var` does not follow the scope


## Lexical Scope


Lexical Scope means that a function can access variables from its parent scope (e.g., parent function).

```js
function parentFunction() {
  let age = 25;
  function innerFunction() {
    console.log(age); // 25
  }
  innerFunction();
}

parentFunction();
```

