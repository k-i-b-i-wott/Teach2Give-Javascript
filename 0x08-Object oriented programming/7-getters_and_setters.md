# Getters and Setters

Getters and setters are methods that allow you to access and modify the value of a private property.

Getters and setters are used to control access to private properties

- Getters (`get`) are used to retrieve the value of a private property

- Setters (`set`) are used to set the value of a private property

Example without setters and getters

```js
class User {
  constructor(name) {
    this.name = name; // Direct access
  }
}

const user = new User("Dennis");
console.log(user.name); // "Dennis"

user.name = 42; // No validation, allows invalid data
console.log(user.name); // 42 (Not ideal)

```

The solution is to use Getters and Setters:

```js
class User {
  constructor(name) {
    this._name = name; // Direct access
  }
  //getter

  get name() {
    return this._name;
  }

  //setters(vaildates and updates the value)

  set name(value) {
    if (typeof value !== "string") {
        console.error("Name must be a string");
        return;
    }
    this._name = value;
  }
}

const user = new User("Dennis");
console.log(user.name); // "Dennis"

user.name = 42; // No validation, allows invalid data
console.log(user.name); // 42 (Not ideal)

```
