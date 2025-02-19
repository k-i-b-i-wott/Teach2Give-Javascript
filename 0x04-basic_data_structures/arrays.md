# Arrays

An array is a collection of elements stored at contiguous memory locations.

An array is a special variable that can hold more than one value.

An array can hold many values under a single name, and you can access these values by referring to an index number.

## Creating an array

You can create in one of the following ways:

- An array literal
- The `new Array()` array constructor

## Using Array literal

```js
const arrayName=[1,2,3,4,5];
```
Example:

```js
const arrayName=["John","Doe", "Biwott"];  // An array of strings
```

You can also nest arrays within arrays(multidimensional arrays)

```js
const arr=[[1,2,3],[4,5,6],[7,8,9]];
```

## Using the `new Array()` array constructor

```js
const arrayName=new Array(1,2,3,4,5);
```
Example:

```js
const students= new Array("John","Doe", "Biwott");      // An array of strings
```
`new Array()` constructor can also be nested

```js
const arr=new Array(new Array(1,2,3),new Array(4,5,6),new Array(7,8,9));
```
Always use array literal to create an array

## Accessing array elements

You can access array elements using their **index number.**

The first element has an index of 0, the second element has an index of 1, and so on.

```js
const students =["John","Doe", "Biwott"];
console.log(students[0]); // Output: John
console.log(students[1]); // Output: Doe
console.log(students[2]); // Output: Biwott
```
## Basic Array methods

### Length of an array

The `length` property returns the number of elements in an array.
The length of an array refers to the number of elements in the array.

```js
const students =["John","Doe", "Biwott"];
console.log(students.length); // Output: 3
```

**`pop()`**

The pop method removes the last item of an array

```js
const students =["John","Doe", "Biwott"];
students.pop();
console.log(students); // Output: ["John", "Doe"]
```
__Note: the pop method returns the element that was removed.__

**`push()`**

The push method adds one or more elements to the end of an array and returns the new length of the array.

```js
const students =["John","Doe", "Biwott"];
console.log(students.push("Sally")); // Output: 4
console.log(students); // Output: ["John", "Doe", "Biwott", "Sally"]
```
You can also add multiple elements using the push method:

```js
const students =["John","Doe", "Biwott"];
console.log(students.push("Sally", "Jane")); // Output: 4
console.log(students); // Output: ["John", "Doe", "Biwott", "Sally", "Jane"]
```
The push method returns the new length of the array.

**`shift()`**

The shift method removes the first item of an array and returns that item.

```js
const students =["John","Doe", "Biwott"];
console.log(students.shift()); // Output: John
console.log(students); // Output: ["Doe", "Biwott"]
```

The shift method returns the element that was removed.

**`unshift()`**

The unshift method adds one or more elements to the beginning of an array and returns the new length of the array.

```js
const students =["John","Doe", "Biwott"];
console.log(students.unshift("Sally")); // Output: 4
console.log(students); // Output: ["Sally", "John", "Doe", "Biwott"]
```
You can add multiple elements using the `unshift` method:

```js
const students =["John","Doe", "Biwott"];
students.unshift("Sally", "Jane");
```

__`at()`__

The at method returns an element at the specified index.

```js
const students =["John","Doe", "Biwott"];
console.log(students.at(0)); // Output: John
console.log(students.at(1)); // Output: Doe
```

**`join()`**

The join method returns a string by concatenating all the elements of an array.

It Behaves just like `toString()` method, in addition, you can specify the separator:

```JS
const students =["John","Doe", "Biwott"];
console.log(students.join("++"));

```
**`concat()`**

The concat method returns a new array by joining two or more arrays.

```js
const students =["John","Doe", "Biwott"];
const arr2=["Sally", "Jane"];
console.log(students.concat(arr2)); // Output: ["John", "Doe", "Biwott", "Sally", "Jane"]
```
**`flat()`**

The flat method converts a multidimensional array into a one-dimensional array.

```js
const students=[
    ["John","Doe", "Biwott"],
    ["Sally", "Jane"],
    ["Alex","Felix"]
];
console.log(students.flat()); // Output: ["John", "Doe", "Biwott", "Sally", "Jane", "Alex", "Felix"]
```

**`inswxOf()`**

The indexOf is used to find the index of an element.
It returns -1 if the element is not found.

```js
const students =["John","Doe", "Biwott"];
console.log(students.indexOf("John")); // Output: 0
```
**`includes()`**

Checks if an element exists in an array.

It returns true if it exits and false if it doesn't

```js
const students =["John","Doe", "Biwott"];
console.log(students.includes("John")); // Output: true
console.log(students.includes("Jane")); // Output: false
```

**`reverse()`**
Reverse the element of an array

```js
const students =["John","Doe", "Biwott"];
console.log(students.reverse()); // Output: ["Biwott", "Doe", "John"]
```