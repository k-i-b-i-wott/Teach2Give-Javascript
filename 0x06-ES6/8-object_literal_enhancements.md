# Object Literal Enhancements


## Computed Property Names
Uses `[]` to create a property name dynamically.

```js

const person = {
    ["first" + "Name"]: "John",
    lastName: "Doe",
    age: 30,

};
console.log(person); // {firstName: "John", lastName: "Doe", age: 30}

```

## Method shorthand

Defining methods in an object without using the `function` keyword.


**Before ES6:**

```JS
const user = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    introduction: function() {
        console.log(`Hello, my name is " ${firstName} ${lastName} and I am ${age}  years old.`);
    },
    
};

user.introduction(); // Hello, my name is John Doe and I am 30 years old.

```

**After ES6:**

```JS
const user = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    introduction() {
        console.log(`Hello, my name is  ${firstName} ${lastName} and I am ${age}  years old.`);
    },
    
};

user.introduction(); // Hello, my name is John Doe and I am 30 years old.
```

## Shorthand Object Property Names
**Before ES6:**

```JS
const firstName = "John";
const lastName = "Doe";
const age = 25;

const user = { firstName: firstName, lastName: lastName, age: age }; //correct
console.log(user); // { firstName: 'John', lastName: 'Doe', age: 25 }

```

**After ES6:**

```JS

const firstName = "John";
const lastName = "Doe";
const age = 25;

const user = { firstName, lastName, age }; // correct
console.log(user); // { firstName: 'John', lastName: 'Doe', age: 25 }

```
