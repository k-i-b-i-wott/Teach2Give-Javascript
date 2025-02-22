-# Polymorphism

Polymorphism allows an entity of an object-oriented code such as a variable or a method to have more than one form.

Polymorphism in object-oriented programming is achieved through:

- **Method overriding**child class provides its own implementation of a method that it has inherited

- **Method overloading:** feature that allows multiple methods in the same class to have the same name but different parameters, not really supported in JavaScript but can be demonstrated.

### Implementing polymorphism with method overriding:


```js

class Math {
  add(number1, number2) {
    return number1 + number2;
  }
}

class Arithmetics extends Math {
  add(number1, number2) {
    if (number1 < 0) {
      console.log("Can only add positive numbers");
    } else if (number2 < 0) {
      console.log("Can only add positive numbers");
    } else {
      console.log(number1 + number2);
    }
  }
}

const arithmetic = new Arithmetics();
arithmetic.add(-5, 5);
arithmetic.add(5, -5);
arithmetic.add(5, 5);

```