# Spread Operator

The spread operator `...` is used to expand an iterable such as an array, into individual elements.


## Use Case of The Spread Operator

### Expanding an array

The spread operator takes the array elements and spreads the individually.

```js

const numbers = [1, 2, 3, 4, 5];

console.log(...numbers); // 1 2 3 4 5

const names=["John", "Doe", "Biwott"];

console.log(...names); // John Doe Biwott

```
### Copying arrays
The spread operator can be used to copy array elements, which helps mutate the original array .

Instead of  :

```js 

const numbers = [1, 2, 3, 4, 5];

const newNumbers = numbers;
newNumbers.push(6);

```

We can do this instead;

```js

const numbers = [1, 2, 3, 4, 5];

const newNumbers = [...numbers];
```

### Merging arrays

```js

const numbers1 = [1, 2, 3];
const numbers2 = [4, 5, 6];
const mergedNumbers = [...numbers1, ...numbers2];

```

### Adding elements from one array to another

```js

const numbers1 = [1, 2, 3];
const numbers2 = [4, 5, 6];
const newNumbers = [...numbers1, ...numbers2];
console.log(newNumbers); // [1, 2, 3, 4, 5, 6]

```


## Copying Objects

```js
const person = {
    name: "John",
    age: 30,
};

const copyPerson = {
    ...person,
    age: 25,    
}
console.log(copyPerson); // {name: "John", age: 25}

```

## Merging

```js
const person1 = {
    name: "John",
};

const person2 = {
    age: 30,
}

const mergedPerson = {
    ...person1,
    ...person2,
};

console.log(mergedPerson); // {name: "John", age: 30}   

```

## Overwriting Properties

```js
const user={
    name: "John",
    age: 30,
    };

    const updatedUser = {
        ...user,
        age: 25,
    };

    console.log(updatedUser); // {name: "John", age: 25}

```
