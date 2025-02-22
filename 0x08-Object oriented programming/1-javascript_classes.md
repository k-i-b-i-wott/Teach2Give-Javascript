# Javascript classes

Javascript classes are a way to create objects in JavaScript. They are the blueprint of an object.


## Creating a class

```js
class ClassName {
    constructor() {
        // constructor
    }
    // methods
}
```

example: 

```js
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    greet() {
        console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
    }
}

const person = new Person("John", 30);
person.greet(); // Output: Hello, my name is John and I am 30 years old.

```
