# Abstraction

Abstraction is a way of hiding the details of a system from the user.

It allows the user to focus on the important parts of the system and ignore the less important parts.

Abstraction is one of the core concepts of object-oriented programming

```js

class BankAccount {
  #balance = 0;

  constructor(owner) {
    this.owner = owner;
  }

  deposit(amount) {
    this.#balance += amount;
    console.log(`Deposited ${amount}. New balance: ${this.#balance}`);
  }

  checkBalance() {
    console.log(`Current balance is: ${this.#balance}`);
  }

  withdraw(amount) {
    if (amount > this.#balance) {
      console.log(`Please enter an amount that matches your balance`);
    } else {
      this.#balance -= amount;
      console.log(
        `Successful withdrawal of ${amount}. New balance: ${this.#balance}`,
      );
    }
  }
}

const account = new BankAccount("John");
account.deposit(500);
account.withdraw(900); // Please enter an amount that matches your balance
account.withdraw(200); // Successful withdrawal of 200. New balance: 300

```