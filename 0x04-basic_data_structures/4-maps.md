# Maps

A map data structure is similar to an object, in that it allows you to store key-value pairs.

However, unlike objects, keys in a map can be of any data type.

## Creating a map

To create a map, use `new Map()`

```js
const myMap = new Map();
```

## Map Methods

### `set(key, value)`

Adds a key value pair to the map or updates if the key-value pair already exists.

```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");
console.log(myMap);

// Map(5) {
//   'firstName' => 'Dennis',
//   1 => 'number',
//   [ 1, 2, 3 ] => 'array',
//   true => 'boolean value',
//   { username: 'the_user' } => 'object'
// }
```

### `get(key)`

Returns the value associated with the specific key in the map or undefined if it doesn't exist.


```js

const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

console.log(myMap.get(1)); // number
console.log(myMap.get("firstName")); // Dennis
console.log(myMap.get("something")); // undefined
```

### `has(key)`

Returns true if the map contains the specified key, otherwise returns false.

```js

const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

console.log(myMap.has(1)); // true
console.log(myMap.has("firstName")); // true
console.log(myMap.has("something")); // false
```

### `delete(key)`

Removes the key-value pair associated with the specified key from the map.

```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

myMap.delete("firstName");
myMap.delete(1);
```

### `clear()`

Removes all key-value pairs from the map.
```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

myMap.clear();

console.log(myMap); // Map(0) {}
```
### `size`

Returns the number of key-value pairs in the map.

```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

console.log(myMap.size); // 5
```
