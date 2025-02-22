# Inheritance

Inheritance allows one class to inherit properties and methods from another class.

This helps in code reusability and hierarchical structuring of objects.

Implemented using the `extends` keyword.

```js
class Animal {
  constructor(numLegs, numEyes) {
    this.numLegs = numLegs;
    this.numEyes = numEyes;
  }

  move() {
    console.log(`Animal looking at the road with ${this.numEyes} eyes`);
    console.log(`Animal moving with ${this.numLegs} legs`);
  }

  eat() {
    console.log(`Animal eating for survival`);
  }
}

class Cow extends Animal {
  constructor(numLegs, numEyes, breed, gender) {
    super(numLegs, numEyes); // calls the parent constructor
    this.breed = breed;
    this.gender = gender;
  }

  sound() {
    console.log(`The ${this.gender} ${this.breed} cow is mooing`);
  }
}

const myCow = new Cow(4, 2, "Guernsey", "Male");
myCow.move();
myCow.eat();
myCow.sound();

```