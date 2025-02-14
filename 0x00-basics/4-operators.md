# Operators

Operators in JavaScript are symbols that perform operations on values **(operands)** .

They are used for calculations, comparisons, and logical operations.

Operators in JavaScript are classified into the following categories:

<ul>

<li>Arithmetic operators: perform basic mathematical operations.</li>
<li>Assignment operators: assign values to variables.</li>
<li>Comparison operators: compare values.</li>
<li>Logical operators: used for boolean logic.</li>
<li>Bitwise operators: perform operations at the binary level.</li>
<li>Ternary operators</li>
<li>Type operators</li>
</ul>


In this chapter, we will go through arithmetic operators, assignment operators, comparison operators and logical operators, we will later on, in this course, go through bitwise, ternary and type operators.


# Arithmetic Operators

These are used to perform mathematical operations.

## + (addition)

Adds two numbers:

```js
let a = 10;
let b = 5;
console.log(a + b); // 15

```

It can also be used with strings to perform string concatenation:

```js

let firstName = "John";
let lastName = "Doe";
console.log(firstName + lastName); // JohnDoe

```


## - (subtraction)

Subtracts the right operand from the left:

```js 

let a = 10;
let b = 5;
console.log(a - b); // 5

```

## * (multiplication)

Calculates the product of two numbers:


```js 

let a = 10;
let b = 5;
console.log(a * b); // 50

```

## / (Division)

```js

let a = 10;
let b = 5;
console.log(a / b); // 2

```

## % (modulus/remainder)

Returns the remainder of the division between the left and right operand.


```js

let a = 10;
let b = 5;
console.log(a % b); // 0

```

## ** (Exponentiation)

```js

let a = 10;
let b = 5;
console.log(a ** b); // 100000

```

## Increment Operator

Increases the variable's value by 1.

It can be used in two ways:
<ul>
<li>Post-increment `(a++)`: returns the original value and then increments it</li>

<li>Pre-increment `(--a)`: increments first then returns the updated value.</li>

</ul>

```js 

let x = 5;
console.log(x++); // 5 (returns first, then increments)
console.log(x); // 6

let y = 5;
console.log(++y); // 6 (increments first, then returns)

```




## Decrement Operator
Decreases the variable's value by 1.

It can be used in two ways:

<ul>
    <li>Post-decrement `(a--)`: returns the original value, then decrements.</li>
    <li>Pre-decrement `(--a)` – decrements first, then returns the updated value.</li>
</ul>  



# Assignment Operators

Used to assign values to variables


= (Simple assignment operator)

Used to assign a value to a variable

```js

let x = 5;

```

## += (Addition assignment operator)


Used to add a value to a variable


```js
let x = 5;
x += 3; // x = x + 3 → 8

```

## -= (Subtraction assignment operator)

Subtracts a value from a variable


```js

let x = 5;
x -= 2; // x = x - 2 → 3

```

## *= (Multiplication assignment operator)

Multiples a variable

```js 

let x = 5;
x *= 2; // x = x * 2 → 10

```


## /= (Division Assignment Operator)

Divides a variable

```js

let x = 15;
x /= 3; // x = x / 3 → 5

```

## Comparison Operators
They are used to compare values and they return true or false.

### == (Equality Operator)
Returns true if the operand on the left is equal to the operand on the right and false otherwise.

```js 

let a = 10;
let b = 5;
console.log(a == b); // false
console.log(a == 10); // true

```
Note: The equality operator ignores the data type of the operands, it only compares the value:


```js 
console.log(10 == "10"); // true


```

## === (Strict equality operator)

Returns true if the operand on the left is equal to the operand on the right and false otherwise.

```js 

let a = 10;
let b = 5;
console.log(a === b); // false
console.log(a === 10); // true

```

Note: The strict equality operator checks the data type as well, not just the values:

```js
console.log(10 === "10"); // false

```

## !`=` (Not equal/Inequality operator)


Returns true if the value on the left is not equal to the value on the right and false otherwise.

It does not consider the data type of the operands.

```js 
let a = 10;
let b = 5;
console.log(a != b); // true
console.log(a != 10); // false

console.log(10 != "10"); // false

```



## `!==` (Strict not equal to/Strict inequality operator)

Returns true if the value on the left is not equal to the value on the right and false otherwise.

It compares the data types of the operands.

```js 

let a = 10;
let b = 5;
console.log(a !== b); // true
console.log(a !== 10); // false

console.log(10 !== "10"); // true

```

## > (Greater than)

Returns true if the operand on the left is greater than the operand on the right and false otherwise.

```js

let a = 10;
let b = 5;
console.log(a > b); // true
console.log(b > a); // false

```

## `< `(Less than)

Returns true if the operand on the left is less than the operand on the right and false otherwise.

```js

let a = 10;
let b = 5;
console.log(a < b); // false
console.log(b < a); // true


```


## `>=` (Greater than or equal to)

Returns true if the operand on the left is greater than or equal to the operand on the right.

```js 

let a = 10;
let b = 5;
console.log(a >= b); // true
console.log(b >= a); // false
console.log(10 >= 10); // true

```

## `<=` (Less than or equal to)
Returns true if the operand on the left is less than or equal to the operand on the right.


```js

let a = 10;
let b = 5;
console.log(a <= b); // false
console.log(b <= a); // true
console.log(10 <= 10); // true


```


# Logical Operators

Used for boolean logic.


## Logical `AND` Operator `(&&)`


The AND operator returns true only if both operands are true; otherwise, it returns false.

```js

console.log(true && true); // true
console.log(true && false); // false


```

## Truth table for the AND operator.

| Expression 1 | Expression 2 | Result |
|:-------------:|:---------:|--------:|
| true        | true        | true   |
| true        | false       | false  |
| false       | true        | false  |
| false       | false       | false  |


# Logical `NOT `operator `(!)`
Used to negate boolean value of an expression, it returns true if the expression is false and returns false if the expression is true.

```js

console.log(!true); // false
console.log(!false); // true

```






















