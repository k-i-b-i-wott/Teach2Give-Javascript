# Promises

Promises are a way to handle asynchronous operations in JavaScript.

It involves the process of **producing** code and **consuming** code.


- **Producing code**: is the code that will take sometimes to complete.

- **Consuming code**: is the code that will wait for the producing code to complete.

A **promise** is an object   links producing code and consuming code.

States of a promise

- **Pending**: initial stage; neither fulfilled nor rejected.
- **Fulfilled** : completed successfully.

- **Rejected** : failed.

## Creating a promise

Created using the `new Promise()` constructor.

The ``new Promise()`` constructor takes two arguments, which is the executor function.

```js
const promise = new Promise((resolve, reject) => {
    // executor function

    let x =1;
    if (x ==1) {
        resolve("success");
    } else {
        reject("error");
    }
    

});

```

## Consuming a promise

Use `.then()` method to handle resolved values and `.catch()` to handle rejected values.

`.then` takes a callback function, which receive  the resolved value of the promise as its arguments.

`.catch` takes a callback function, which receive the rejected value of the promise as its arguments.

```js
let myPromise = new Promise(function (resolve, reject) {
  let x = 5;
  if (x === 1) {
    resolve("x is 1");
  } else {
    reject("x is not 1");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });

  ```

  The `.finally()` method is used to execute a function regardless of whether the promise is resolved or rejected.

  ```js
  let myPromise = new Promise(function (resolve, reject) {
  let x = 1;
  if (x === 1) {
    resolve("x is 1");
  } else {
    reject("x is not 1");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  })
  .finally(() => {
    console.log("It was nice working with this promise");
  });

  ```


  ### Returning a promise from a function

```js
function fetchUser() {
  return new Promise(function (resolve, reject) {
    let error = false;
    if (error === true) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

fetchUser()
  .then((user) => {
    console.log(`Username: ${user.username}, Role: ${user.role}`);
  })
  .catch((error) => {
    console.log(error);
  });

  ```

  