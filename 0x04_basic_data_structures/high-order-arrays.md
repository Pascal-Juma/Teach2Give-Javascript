# High Order Array Methods

- ### They allow us to apply functions to elements directly simplifying operations on arrays.

### They include:

### 1. `forEach`
- ### Executes a function on each array element.

```js
const numbers =[1, 2, 3, 4, 5];

numbers.foreach((num) = >{
    console.log(num * 2);
});
```
### output: 
```js
2, 4, 6, 8, 10
```

### 2. `map`
- ### It creates a new array with the results of calling a function on every element in the calling array.
```js
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map((num) => num * 2);
console.log(doubled);
```
### output:
```js
[2, 4, 6, 8, 10]
```
### 3. `filter`
- ### It creates a new array with all elements that pass the test implemented by the provided function.
```js
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter((num) => % 2 === 0);
console.log(evenNumbers); 
```
### output:
```js
[2, 4]
```
### 4. `reduce`
- ### It results in a single output value by executing a reducer function on each element of the array.
```js
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum);
```
### output:
```js
15
```

### 5. `find`
- ### It returns the value of the first element in the array that satisfies the provided testing function, otherwise undefined.
```js
const numbers = [1, 2, 3, 4];
const found = numbers.find((num) => num === 3);
console.log(found);
```
### output:
```js
3
```
### 6. `findIndex`
- ### Returns the index of the first element that matches a condition.

```js
const numbers = [10,20, 30, 40, 50];

const index = numbers.findIndex((num) => num > 25);
console.log(index);
```
### output:
```js
2
```
### 7. `some`
- ### Checks if at least one element passes a condition.
```js
const numbers = [1, 3, 5, 7];

const hasEven = numbers.some((num) => num % 2 === 0);
console.log(hasEven);
```
### output:
```js
false
```
### 8. `every`
- ### Examines if all elements in an array pass a condition.
```js
const numbers =[2, 4, 6, 8];

const allEven = numbers.every((num) => num % 2 === 0);console.log(allEven);
```
### output:
```js
true
```