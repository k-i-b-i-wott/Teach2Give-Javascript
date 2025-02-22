# Introduction to `fetch` and HTTP Requests

`fetch` is a JavaScript function that allows you to make HTTP requests to a server.


It helps the code send and receive data from websites or APIs

`fetch` is a **lightweight** and **simple** way to make HTTP requests in JavaScript

`fetch` sends a request to a website (server), and the server responds with some data.

## HTTP Requests

HTTP is a protocol used for sending and receiving data over the internet.

HTTP requests are made using the `fetch` function.

Types of request:

- GET: a computer asks for data

- POST: a computer sends data

- DELETE: a computer deletes data

- PUT: a computer updates data

## Making a simple fetch request

```js

fetch("https://jsonplaceholder.typicode.com/users")
  .then(function (response) {
    return response.json();
  })
  .then(function (data) {
    console.log(data);
  })
  .catch(function (error) {
    console.log("There was an error");
    console.log(error);
  });

  ```
### Explanation

- The `fetch` function is used to make a request to the server.
`fetch('https://jsonplaceholder.typicode.com/users')` makes a request to the server at the specified URL.


```js
.then(function (response) {
    return response.json();
})
```

- The `then` function is used to handle the response from the server.

```js
.then(function (data) {
    console.log(data);
})
```
Receives data from the previous step and displays it in the user's console.

```js
.catch(function(error)){
  console.log("There was an error");
  console.log(error);
}

```
if the request fails, the `catch` function is used to handle the error.

## Using async await for easier syntax
Use async await for cleaner approach

```js

async function getData() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/users");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.log("There was an error");
    console.log(error);
  }
}

getData();
```

## Handling HTTP Errors

```js
async function getData() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/users");
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.log("There was an error");
    console.log(error);
  }
}

getData();

```
