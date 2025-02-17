# Scope

Scope in JavaScript defines the accessibility of variables.

### They include:

## 1. Global Scope
This is a variable declared outside any function. It can accessible anywhere in the program.

```javascript
let score = 70;

function gradeScore() {
    console.log(score); // accessible inside function
}

gradeScore(); // 70
console.log(score); // accessible outside function too
```

Output:
```
70
70
```

## 2. Function Scope
These are variables that are declared inside and can only be accessed within it. 

```javascript
function gradeScore() {
    let score = 70;
    console.log(score); // works inside the function
}

console.log(score); // ReferenceError: score is not defined
```

## 3. Block Scope
Here we use the the `let` and `const` keywords to declare variables inside a block of code, however the `var` keyword does not follow block scope.


A block is any code inside curly brackets `{}` (e.g., in `if`, `for`, `while` statements).

```javascript
if (true) {
    let score = 40;
    console.log(score); // works inside the block
}
console.log(score); // score is not defined
```

## 4. Lexical Scope
A function can access variables from its parent scope.

```javascript
function parentFunction() {
    let score = 40;
    function innerFunction() {
        console.log(score); // 40
    }
    innerFunction();
}

parentFunction();
```
Output:

```
40
```