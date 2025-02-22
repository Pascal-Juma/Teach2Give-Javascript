# Template literals

### Template literals makes strings more flexible and readable.

### They allow:

- ### Multi-line strings without \n.
- ### String interpolation.

- ### Embedded expressions.

## String interpolation: Injecting variables into strings

### Before template literals:
```js
const username = "Dennis";
const age = 25;

console.log("My name is " + username + " and I am " + age + " years old.");
// My name is Dennis and I am 25 years old.
```
### With template literals:
```js
const name = "Dennis";
const age = 25;

console.log(`My name is ${name} and I am ${age} years old.`);
// My name is Dennis and I am 25 years old.
```
## Multi-line strings
### Before
```js
const multiLine = "This is line 1\n" + "This is line 2\n" + "This is line 3";

console.log(multiLine);
/*
This is line 1
This is line 2
This is line 3
*/
```
### With ES6
```js
const multiLine = `This is line 1
This is line 2
This is line 3`;

console.log(multiLine);
/*
This is line 1
This is line 2
This is line 3
*/
```
## Expressions inside template literals
```js
let a = 10;
let b = 20;

function product(number1, number2) {
  return number1 * number2;
}

console.log(
  `The sum of ${a} and ${b} is ${a + b} and the product is ${product(a, b)}`,
);
```