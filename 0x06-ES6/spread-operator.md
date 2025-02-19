# Spread Operator
### The spread operator (`...`) expands elements into individual elements.

## Use Cases of The Spread Operator
### 1. Expanding an array
### Eg.
```js
const numbers = [1, 2, 3];
console.log(...numbers); // 1 2 3

const names = ["John", "Doe"];
console.log(...names); // John Doe
```
### 2. Copying arrays
### Eg.
```js
const original = [1, 2, 3];
const copy = [...original];
```
### 3. Merging arrays
### E.g 
```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const merged = [...arr1, ...arr2];

console.log(merged); // [1, 2, 3, 4, 5, 6]
```
### 4. Adding elements from one array to another
### Eg
```js
const numbers = [2, 3, 4];
const newNumbers = [1, ...numbers, 5];

console.log(newNumbers); // [1, 2, 3, 4, 5]
```
### 5. Copying objects
### Eg
```js
const person = { name: "John", age: 25 };
const copy = { ...person };

console.log(copy); // Output: { name: "John", age: 25 }
```
### 6. Merging objects
### Eg.
```js
const obj1 = { name: "John" };
const obj2 = { age: 25 };
const merged = { ...obj1, ...obj2 };

console.log(merged); //  { name: "John", age: 25 }
```
### 7. Overwriting Properties
```js
const user = { name: "John", role: "User" };
const updatedUser = { ...user, role: "Admin" };

console.log(updatedUser); // { name: "John", role: "Admin" }
```