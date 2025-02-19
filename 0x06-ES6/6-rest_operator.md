# Rest Operator

The rest operator `...` is used to collect all the remaining elements of an iterable into an array.


## Use Case of The Rest Operator

### Rest in function parameters

Used when a function has multiple parameters but we don't know how many arguments will be passed.

```js
function myFunction(...numbers){
    console.log(numbers);
}

add(5,6);
add(9,8,7);
add(2,3,4,);

```

