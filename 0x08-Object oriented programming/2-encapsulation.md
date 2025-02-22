# Encapsulation
It is a way of bundling data and methods that operate on data into a single unit while restricting direct access to the data.

Encapsulation is one of the core concepts of object-oriented programming
It can be achieved by using **private properties** and **getters/setter**.

example;

```js

class BankAccount {
    #balance = 0;
    constructor (owner) {
        this.owner = owner;
    }

    deposit(amount) {
        this.#balance += amount;
        console.log(`Deposited ${amount}, total balance is ${this.#balance}`);
    }

}
const account = new BankAccount("Dennis");
account.deposit(100);
account.checkBalance();
```

`#balance` is private and cannot be accessed directly from outside the class
`deposit()` and `checkBalance()` is a public method that can be called from outside the class

`checkBalance()` is a public method that can be called from outside the class