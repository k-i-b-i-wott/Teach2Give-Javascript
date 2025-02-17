# Loops

Loops enable you to execute a block of code multiple times.

The basic loops in  Javascript are:

- for loop
- while loop
do while loop


## for loop

Used when the number of times the block of code should be executed is known.

The syntax is as follows:

```js
for (initialization; condition; update) {
    // code
}
```
- _Initialization_ is used to initialize the variable used in the loop.

- _Condition_ is used to evaluate the condition of the initial variable, if the condition returns true, the loop starts over again, if the condition returns false, the loop ends.
- _Update_ is used to update the initializationvariable.

```js
for (let a = 1; a <= 10; +=2) {
    console.log("Iteration:", a);
}
```

## While loop

Runs as long as a specific condition remains true.

```js
while (condition){
    //code block to be executed if condition is ture
}
```


```js
let num = 1;

while (num <= 5) {
  console.log("Number ", num);
  num++;
}

```

## do while loop

Executes the loop at least once, even if the condition is `false` from the end.


```js

do{
    // block of code that will be executed at least once even if condition is false
} while (condition)

```

```js

let a = 1;

do {
  console.log("a ", a);
  a++;
} while (a <= 5);


```


## break and continue statements

`break` and `continue` statements are keywords that are always used within a loop


### `break` statement

The purpose of a break statement is used when the running loop needs to be terminated whenever any particulr condition occurs.

Whenever a `break` statement occurs, the loop breaks and stops executing.

The `break` statement exits the loop completely.


``` js

for (let i = 0; i < 5; i++) {
  if (i == 4) {
    break;
  }
  console.log(i);
}

```

### `continue ` statement

The `continue` statement is used when we want to skip a particular iteration.

Whenever we write `continue` statement, the whole code after that statement is skipped and the loop will go for the next iteration.

The `continue` statement skips the current iteration and moves on to the next iteration.


```js
for (let i = 0; i < 5; i++) {
  if (i == 5) {
    continue;
  }
  console.log(i);
}

```