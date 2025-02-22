# Static Methods and Properties
Static methods and static properties belong to a class itself rather than its instances.

They can be accessed without creating an object of the class.


# Static Methods

Static methods are methods that are not associated with any particular instance of a class.


```js
class Math {
    static add(number1, number2) {
       
       return number1 + number2;
    }
    static subtract(number1, number2) {
        return number1 - number2;
    }
}

console.log(Math.add(5, 4));
console.log(Math.subtract(5, 4));


const math= new Math();
//console.log(math.add(5, 4)); error: mathh.add is not a function
```

# Static property

Variable that belongs to a class

```js

class Counter {
  static count = 0; // Static property

  static increment() {
    Counter.count++; // Accessing the static property
  }

  static getCount() {
    return Counter.count;
  }
}

// Accessing static property without an instance
console.log(Counter.getCount()); // 0

Counter.increment();
Counter.increment();

console.log(Counter.getCount()); // 2
```
