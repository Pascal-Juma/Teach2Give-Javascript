# Maps

### A map allows you to store key-value pairs of any data type.

## Creating a map

```js
const myMap = new Map();
```

## Map methods

### a. `has(key)`

```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

console.log(myMap.has("firstName")); //output ->  true
console.log(myMap.has("middlename")); // output -> false
```

### b. `set(key, value)`

```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");
console.log(myMap);
``` 
### output:
```js
// Map(5) {
//   'firstName' => 'Dennis',
//   1 => 'number',
//   [ 1, 2, 3 ] => 'array',
//   true => 'boolean value',
//   { username: 'the_user' } => 'object'
// }
```

### c. `get(key)`

```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

console.log(myMap.get(1)); // output -> number
console.log(myMap.get("firstName")); //output ->  Dennis
console.log(myMap.get("something")); //output -> undefined
```

### d. `clear()`

```js
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

myMap.clear();

console.log(myMap); //output -> Map(0) {}
```

### e. `delete(key)`

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

### f. `size`

```javascript
const myMap = new Map();
myMap.set("firstName", "Dennis");
myMap.set(1, "number");
myMap.set([1, 2, 3], "array");
myMap.set(true, "boolean value");
myMap.set({ username: "the_user" }, "object");

console.log(myMap.size); // 5
```