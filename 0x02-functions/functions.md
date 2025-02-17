# Functions

A function is a block of code that performs a specific task.

Functions help in writting modular, maintainance


**In Javascript, functions are firts-class citizens; this means that they can be assigned to variables, passedas arguments, return from other functions, stored in data structures and even created dynamically**

Basic syntax for Javascript Function:

```js 
function functionName() {
  // function body
}
```
```js

function printHello() {
  console.log("Javascript is fun");
}

```

To use a function, you must **call/invoke** the function as shown:

```js
function printHello() {
  console.log("Javascript is fun");
}

// calling/invoking a function
printHello();

```

# Parameters vs Arguments

A parameter is a variable declared in a function definition  and acts as a placeholder for the value that will be passed when the function is called.

An argument is a value that is passed to a function when it is called, it provides the data that the function needs to perform its task.

```js

function printName(name) {
  console.log(`Hello ${name}`); // Hello  + name);

}

printName("John"); // Hello John

``` 
## Function Return Values

A function can return a value using the `return` keyword.

```js

function sum(number1, number2) {
  return number1 + number2;
}
 let result = sum(10, 20);
 console.log(result); // 30

```

 # Categories of Functions

 In programmming, functions can be classified into the following categories:

 - Functions that don't take parameter(s) and return a value
 - Functions that take parameter(s) and return a value
 - Functions that don't take parameter(s) but return a value
 - Functions that take parameter(s) but don't return a value



## Functions that don't take parameter(s) and return a value

```js

function printHello() {
  console.log("Javascript is fun");
  }

 printHello(); // Javascript is fun

```




 ## Functions that don't take parameter(s) and don't return a value

 As the name suggests, these functions don't take any parpmeter(s) and return a value.

 ```js  
 function add() {
   let num1 = 10;
   let num2 = 20;
   console.log(num1 + num2);
     
 }
 }

 add();      

 ```

 ## Functions that take parameter(s) and return a value
 These functions don't take any parpmeter(s) and return a value.

 ```js
 function add() {
    let a =55;
    let b =72;
    return a + b;
     
 }

 let result = add();
 console.log(result); // 127

 ```

 ## Functions that  takes parameter(s) but don't return a value

 ```js
 function multiply(a,b) {
    return a * b;
     
 }

 console.log(multiply(12,17)); 

 ```


 # Types of functions in JavaScript

 Javascript has the following types of functions:

 - Function declaration
 - Function expression/anonymous function
 - Arrow function
 - Immediately invoked Funstion Expression (IIFE)
 - Callback function


 ## Function declaration

 ```js
 function add(a,b){
    console.log(a + b);
 }
 add(10,20);

 ```

 ## Function expression/anonymous function
 Involves saving a function to a variable and then calling it.

 ```js
 let add = function(a,b){
    console.log(a + b);
 }
 add(10,20);

 ```

 ## Arrow function

 Arrow functions were introduced in ES6 and are used to simplify how we write functions.

 ```js
 let add = (a,b) => {
     return a + b;
 }
 console.log(add(10,20));

 ```
 **If arrow function has only one line in the body, we can get rid of the curly braces**

 This means that instead of:

 ```js
 let add = (a,b) => {
     console.log(a + b);
 }
 add(10,20);

 ```

We can write it as:

 ```js
 let add = (a,b) => console.log(a + b);
 add(10,20);

 ```

 **If an arrow function has only one line of code in the body and that line happens to be a return statement, we can get rid of the return keyword:**

 ```js
 let add = (a,b) => a + b;
 console.log(add(10,20));

 ```
 **If an arrow function has only one parameter, we can get rid of the parenthesis:**

 ```js
 let square = a => a * a;
 console.log(square(10));

 ```    
 ## Immediately invoked Funstion Expression (IIFE)

 These functions are executed immediately after they are defined.

 ```js

 (function() {
   console.log("Javascript is fun");
 })

 These functions can also take parameters.

 ```js

 (function(a,b) {
 let sum = a + b;
 let product= a * b;
 console.log(`Sum: ${sum}, Product: ${product}`);

 })(10,20);

 ```

 ## Callback function

 A callback function is a function passed as an argument to another function.

 ```js

 function printName(name,callback) {
  console.log(`Hello ${name}`); // Hello  + name);
  callback();

}

printName("John", function() {
  console.log("Welcome to tech");
})




