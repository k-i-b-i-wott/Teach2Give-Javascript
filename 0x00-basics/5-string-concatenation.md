# String Concatenation

String concatenation is the process of joining two or more strings together.

JavaScript provides multiple ways to concatenate strings.

# 1. Using the `+` Operator

You can use the + operator to join strings together.

```js

let firstName = "John";
let lastName = "Doe";
let fullName = firstName + lastName;
console.log("My full name is " + fullName);

```


# 2. Using the += operator to append to an existing string

```bash
let message = "Hello ";
message += "Dennis.";
console.log(message);P

```


# 3.Using Template Literals

Template literals (introduced in ES6) use backticks (`) and '${}' placeholders for variables.
```js

let firstName = "John";
let lastName = "Doe";
console.log(`My name is ${firstName} ${lastName}`);


```