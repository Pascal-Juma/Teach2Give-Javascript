# Functions In JavaScript

A functon is a block of code that helps in writing modular, maintainable, and reusable code.

## Basic Syntax

```javascript
function functionName() {
    // function body
}
```

Example:

```javascript
function printHello() {
    console.log("Hello, world");
}
```

You must call the function to use it.

```javascript
function printHello() {
    console.log("Hello, world");
}

// calling/ a function
printHello();
```

## Parameters vs Arguments

A parameter acts as a placeholder for the value that will be passed to the function.

An argument is the actual value that is passed to the function.


```javascript
function greet(name) { // name is a parameter
    console.log(`Hello ${name}`);
}

greet("John Doe"); // John Doe is an argument
```

## Function Return Values

 We use the `return` keyword.

```javascript
function add(number1, number2) {
    return number1 + number2;
}

let sum = add(35, 23);
console.log(sum);
```

## Categories of Functions

### 1. Functions that don't take parameter(s) and don't return a value

```javascript
function add() {
    let a = 40;
    let b = 70;
    console.log(a + b);
}

add();
```

### 2. Functions that don't take parameter(s) but return a value

```javascript
function add() {
    let a = 40;
    let b = 70;
    return a + b;
}

console.log(add());
```

### 3. Functions that take parameter(s) but don't return a value


```javascript
function add(a, b) {
    console.log(a + b);
}

add(5, 3);
```

### 4. Functions that take parameter(s) and return a value

```javascript
function add(a, b) {
    return a + b;
}

console.log(add(5, 3));
```

## Types of Functions in JavaScript

### 1. Function Declaration

```javascript
function add(a, b) {
    console.log(a + b);
}

add(5, 2);
```

### 2. Function Expression/Anonymous Function

```javascript
let add = function (a, b) {
    console.log(a + b);
}

add(5, 2);
```

### 3. Arrow Functions

```javascript
let add = (a, b) => {
    return a + b;
}

console.log(add(5, 2));
```

Get rid of the curly braces if function has only one line

```javascript
let add = (a, b) => console.log(a + b);

add(5, 2);
```

Get rid also of the `return` keyword if function has only one line

```javascript
let add = (a, b) => a + b;

console.log(add(5, 2));
```

Get rid of the parenthesis also if function has only one parameter

```javascript
let square = number => number * number;

console.log(square(4)); // 16
```

### 4. Immediately Invoked Function Expressions (IIFE)

```javascript
(function () {
    console.log("Hello, World!");
})();
```


```javascript
(function (d, p) {
    let sum =  + p;
    let product = d + p;
    console.log(`The sum of ${d} and ${p} is ${sum}`);
    console.log(`The product of ${d} and ${p} is ${product}`);
})(8, 9);
```

### 5. Callback Functions

Functions passed as arguments to other functions.

```javascript
function greet(name, callback) {
    console.log(`Hello ${name}`);
    callback();
}

greet("Abraham", function () {
    console.log("Welcome Friends");
});
```