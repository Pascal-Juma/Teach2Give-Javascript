# JavaScript Variables

## Understanding Variables
A **variable** in JavaScript acts as a named storage unit that holds a value, which can be retrieved and manipulated later. Think of it like a labeled box where you can store different kinds of data—numbers, text, lists, or even functions.

A **constant** is similar but holds a value that remains unchanged throughout the program.

## Declaring Variables in JavaScript
JavaScript provides three main ways to declare variables:

1. **`var`** – The old way, now mostly avoided due to unpredictable behavior in modern applications.
2. **`let`** – The preferred method for variables whose values might change.
3. **`const`** – Used when a value should remain constant and never be reassigned.

### Example:
```js
let age = 25; // A variable named "age" storing the value 25
const userName = "Dennis"; // A constant holding a text value
var city = "Tokyo"; // Old way of declaring variables (not recommended)
```

## Updating Variables
Variables declared with `let` and `var` can be reassigned.

```js
let counter = 0;
counter = 1;
console.log(counter); // Output: 1
```

However, attempting to modify a `const` variable results in an error:

```js
const PI = 3.14159;
PI = 3.14; // This will throw an error
```

## Declaring vs. Initializing Variables

### Declaring a Variable
Declaring a variable means introducing it without giving it a value. When accessed before initialization, it returns `undefined`.

```js
let status;
console.log(status); // Output: undefined
```

### Initializing a Variable
Initialization involves assigning a value at the time of declaration.

```js
let age = 30; // Declared and initialized
console.log(age); // Output: 30
```

**`const` must always be initialized immediately upon declaration.**

## Rules for Naming Variables

### Allowed Naming Conventions:
- Variable names must start with a **letter**, an **underscore (_)**, or a **dollar sign ($)**.
- They can only contain **letters, numbers, underscores, and dollar signs**.
- Variable names are **case-sensitive** (`name` and `Name` are different).
- Multiple-word variable names should follow **camelCase**.

#### Examples:
```js
let userName = "John";
let _score = 100;
let $price = 47.00;
```

### Avoid These Mistakes:
```js
let 1stPlace = "Eliud"; //  Cannot start with a number
let let = "Farming"; // "let" is a reserved keyword
let total amount = 100; //  Spaces are not allowed
```

## Case Sensitivity in Variables
JavaScript treats lowercase and uppercase letters as different characters:

```js
let Score = 70;
let score = 40;
console.log(Score); // 70
console.log(score); // 40
```

## Writing Clear & Meaningful Variable Names
To improve readability, always use **descriptive and self-explanatory** names.

 **Good Examples:**
```js
let studentScore = 70;
let schoolFees = 27000;
let hasClearedFees = true;
```

**Bad Examples:**
```js
let x = "results"; // Unclear what "x" represents
let tp = 150;   // Ambiguous name
```

By following these best practices, your JavaScript code will be easier to understand and maintain.

