# Consuming Promises with Async/Await

`async/wait` is a syntax that allows you to consume promises in a more readable and concise way.

`async/wait` is used in functions that consume a promise.

```js
function fetchUser() {
  return new Promise(function (resolve, reject) {
    let error = true;
    if (error === true) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

async function processUser() {
  const user = await fetchUser();
  console.log(user);
}

processUser();


```


## Handling errors in async/await

`async/await` has the ability to handle errors in a synchronous way using `try...catch`.

```js

function fetchUser() {
  return new Promise(function (resolve, reject) {
    let error = true;
    if (error === true) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

async function processUser() {
  try {
    const user = await fetchUser();
    console.log(user);
  } catch {
    console.log("Err");
  }
}

processUser();


```

The catch block can also receive error:


```js

function fetchUser() {
  return new Promise(function (resolve, reject) {
    let error = true;
    if (error === true) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

async function processUser() {
  try {
    const user = await fetchUser();
    console.log(user);
  } catch (error) {
    console.log(error);
  }
}

processUser();

```
` try...catch` also has a `finally` block:

```js
function fetchUser() {
  return new Promise(function (resolve, reject) {
    let error = true;
    if (error === true) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

async function processUser() {
  try {
    const user = await fetchUser();
    console.log(user);
  } catch (error) {
    console.log(error);
  } finally {
    console.log(`Process completed`);
  }
}

processUser();

```

