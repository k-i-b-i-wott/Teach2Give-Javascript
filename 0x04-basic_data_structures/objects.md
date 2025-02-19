# Objects

In JavaScript, an object is a collection of key-value pairs.

It is a data structure that stores values as a collection of key value pairs.

The key must always be a string, and the value can be of any type.

Keys are also referred to as **properties**.

Objects are one of the most fundamental data structures in JavaScript.

A function inside an object is called a **method**.


## Creating Objects

Javascript provides the following ways to create objects:

- Object literal
- Using `new object()`
- Using a constructor function

## Using Object Literal

The simplest way to create an object is to use curly braces, this is referred to sa **object literal**.

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};
```
### Using `new Object()`

`new object()` creates an empty object. It's functionally equivalent to object literal but rarely used in modern Javascript.

```js
const student = new Object();
student.firstName = "John";
student.lastName = "Doe";
student.age = 25;
student.isStillStudying = true;
student.greet = function () {
    
    console.log("Hello, World!");
};
```
### Using Constructor Function
A constructor function in JavaScript is a regular function used with the `new` keyword to create multiple objects with shared properties and methods.

```js
function Student(firstName, lastName, age, isStillStudying) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.age = age;
  this.isStillStudying = isStillStudying;
  this.greet = function () {
    console.log("Hello, World!");
  };
}

const student = new Student("John", "Doe", 25, true);
```
For most of the time, always opt for object literals as a mean of creating objects.


## Accessing Object Properties

There are two ways of accessing object properties:

- Dot notation

- Bracket notation

### Dot notation


Dot notation allows access to an object's properties using a dot `(.)` followed by the property name.

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(student.firstName); // Output: "John"
console.log(student.lastName); // Output: "Doe"
```

### Bracket notation

Bracket notation accesses an object's properties using square brackets (`[]`) with the property name as a string.`

It’s useful for dynamic keys or properties with special characters.

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(student["firstName"]); // Output: "John"
console.log(student["lastName"]); // Output: "Doe"
```


##  Modifying Object Properties

####nAdding new properties

You can ude the dot or bracket to add new properties to an object.

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
  };

  student.city = "New York";
  student.country = "USA";

  ```

  #### Updating a property

  ```js
  const student = {
    firstName: "John",
    lastName: "Doe",
    age: 25,
    isStillStudying: true,
    greet: function () {
      console.log("Hello, World!");
    },
    };
    
    student.age = 26;
    student["isStillStudying"] = false;

```

    ### Deleting a property

 Use `delete` keyword to remove a property

 ```js
 const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
      
    console.log("Hello, World!");
  },
  };
  
  delete student.age;

  ```

  ## Checking properties in an object

To check if a certain property is available in an object, you can use:

- The `in` keyword.

- The `hasOwnProperty()` method.

### The `in` keyword

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log("firstName" in student); // true
console.log("middleName" in student); // false
```

### The `hasOwnProperty()` method

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(student.hasOwnProperty("firstName")); // true
console.log(student.hasOwnProperty("middleName")); // false
```

## Object Methods

#### `object.keys(objectName)`

Returns an array containing all the keys of an object

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(Object.keys(student));

```


#### `Object.values(objectName)`

Returns an array containing all the values of an object

```js 
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(Object.values(student));
// [ 'John', 'Doe', 25, true, [Function: greet] ]
```
#### `Object.entries(objectName)`

`Object.entries()` returns an array of key-value pairs from an object, making it useful for iteration.

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(Object.entries(student));
// [
//     [ 'firstName', 'John' ],
//     [ 'lastName', 'Doe' ],
//     [ 'age', 25 ],
//     [ 'isStillStudying', true ],
//     [ 'greet', [Function: greet] ]
// ]
```
## Object.freeze(objectName)

Freezes an object, preventing new properties from being added to it and existing ones from being removed, it also prevents an object from modification.

```js

const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

Object.freeze(student);
student.middleName = "Smith"; // won't work
```

## Iterating over an object using the
 #### `for .. in` **loop**
 You can use `for .. in` loop to iterate over an object as shown:

```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

for (let key in student) {
  console.log(key)
}
```
The `for .. in` loop can also be used to loop over arrays.

