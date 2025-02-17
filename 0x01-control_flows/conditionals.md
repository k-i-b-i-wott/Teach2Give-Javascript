# Conditionals

Conditionals allow you to execute different blocks of code based on specific conditions.

Condtitional statements in Javascript are:

- if statement  
- if else statement
- if else ladder
- switch statement

## if statement

The if statement is used to execute a block of code if specified condition is true.  
Tha syntax is as follows:

```javascript
if (condition){
    //Add a block of code to be executed if the condition is true
}
```

Example in code:

```js
let marks=72;
if(marks > 70){
    console.log("You're grade is A")
}
```

## if else statement

Executes the code in the `if` block when the condition is true, if the condiion is false, the code inside the else block gets executed.

```js   
if(condition){
    // block of code to be executed if the condition is true

} else{
// block of code to be executed if the condition is false
}
```

Example of code:

```js
let marks =72
if (marks >50){
    console.console.log(`Your grade is above average `);
    
} else {
    console.log(`Your grade is below average`)
}
```
## if else ladder
Used when multiple conditions need to be checked sequentially.  

The syntax is as follows:

```js
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if condition1 is false and condition2 is true
} else {
  // block of code to be executed if both condition1 and condition2 are false
}
```

Example of code:
``` js

let score = 85;
if (score>= 90) {
  console.log("Your score is : A");
} else if (score >= 80 && score < 90) {
  console.log("Your score is: B");
} else if (score>= 70 && score < 80) {
  console.log("Your score is: C");
} else {
  console.log("Your score is Fail");
}
```

# Switch statement  

Used when a variable has multiple possible values. It's cleaner than multiple `if...else` conditions  

The syntax is as follows  

```js

switch (expression) {
  case item1:
    // block of code to be executed if expression === value1
    break;
  case item2:
    // block of code to be executed if expression === value2
    break;
  default:
  // block of code to be executed if expression doesn't match any case
}
```

Example of code:

```js
    let month='January'
    switch(month){
        case "January":
            console.log("Start of the Year").
            break:
        case "May":
            console.log("Winter is approaching");
            break:
        
        case "August":
            console.log("The winter is almost over")
            break;
        case "December":
            console.log("Festive season");
            break;
        default:
            console.log("It's a reqular day.");
   }

```

# Ternary Operator

The ternary operator provides a concise way to write if-else statements in a single line

The syntax is:

```js
condition ? expression if condition is true : expression if condition is false
```

Example in code:

```js

const age=25;
age>18? console.log("You are an Adult"): console.log("You are a child");
```





