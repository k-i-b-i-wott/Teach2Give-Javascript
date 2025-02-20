# Callbacks

Callbacks are one of the solutions for asynchronous programming in JavaScript.

Let's say you are building a web application where you need to fetch user data from a database or an API. You might have written your code like this:

```js
function fetchData() {
    let data = { username: "John Doe", role: "Admin" };
    return data;
}

function showData(data) {
    console.log(`Username is ${data.username} and role is ${data.role}`);
}

const userData = fetchData();
showData(userData);

```
`fetchData()` retrieves user data and returns it immediately

`showData(userData)` then logs the user details.

This works **Fine for synchronous**, where `fetchData` instantly provides the data. But what if fetching data time, like when calling an API or reading from a database.

```js
function fetchData(){
    setTimeout(()=>{
        let data ={
            username: "John Doe",
            role: "Admin"
        };
        return data;
    },200);
}
function showData(data){
    console.log(`Username is ${data.username} and role is ${data.role}`);
}

const userData = fetchData();
showData(userData);

```

`setTimeout()`delays the execution of the function, making it asynchronous. This means that the `fetchData` function will not return the data immediately, but instead, it will wait for 200 milliseconds before returning the data.

`fetchData()` does not wait for the data to e ready--it returns immediately. `showData()` then logs the user details.
When `showData(userData)` runs, userData is `undefined`.

#### **The solution here is to use Callbacks**

A **callback function*** is a function passed as an argument to another function,
ensuring that execution happens only after the asynchronous operation is complete.


```js
function fetchData(callback) {
    setTimeout(() => {
        let data = {
            username: "John Doe",
            role: "Admin"
        };
        callback(data);
    }, 2000);
}


fetchData(function (data)){
    console.log(`Username is ${data.username} and role is ${data.role}`);
}
```


Assuming we are fetching data with multiple data points:

- fetch user data (e.g., username and role)

- Fetch user's posts after getting user data

- Fetch comments on a post after retrieving posts

- Display all the data after everything is fetched.

- Using callbacks, your code will look like this:


```js
function fetchUser(callback) {
  setTimeout(() => {
    console.log("Fetched user data");
    let user = { username: "John Doe", role: "Admin" };
    callback(user);
  }, 2000);
}

function fetchPosts(user, callback) {
  setTimeout(() => {
    console.log(`Fetched posts for ${user.username}`);
    let posts = ["Post 1", "Post 2", "Post 3"];
    callback(posts);
  }, 2000);
}

function fetchComments(post, callback) {
  setTimeout(() => {
    console.log(`Fetched comments for ${post}`);
    let comments = ["Nice post!", "Great work!", "Interesting read"];
    callback(comments);
  }, 2000);
}

// Callback Hell (Nested Callbacks)
fetchUser((user) => {
  fetchPosts(user, (posts) => {
    fetchComments(posts[0], (comments) => {
      console.log(`User: ${user.username}, Role: ${user.role}`);
      console.log(`Posts: ${posts}`);
      console.log(`Comments on first post: ${comments}`);
    });
  });
});

```

The problems with the above code are:

- The indentation (callback hell) keeps increasing making the code harder to read.

- The code is hard to maintain and debug.

- The code is hard to test.

- The code is hard to reuse.