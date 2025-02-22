# JavaScript Data Types

JavaScript includes data types which includes:

## 1. String
A **string** is used to represent text and is enclosed in single (`'`), double (`"`), or template literals (`` ` ``).

```js
let city = "Tokyo";
let country = 'Japan';
let location = `Tokyo, Japan`;
```

## 2. Number
JavaScript has a single **Number** type for both integers and floating-point numbers.

```js
let age = 30; // Integer
let height = 175.5; // Decimal
let invalidNumber = NaN; // Not a Number (result of an invalid operation)
```

## 3. Boolean
A **boolean** represents a logical value and can be either `true` or `false`. It is often used in conditional statements to control program flow.

```js
let isActive = true; // The entity is active
let isVerified = false; // The entity is not verified
```

## 4. Undefined
A variable is `undefined` when it has been declared but not assigned a value.

```js
let paymentStatus;
console.log(paymentStatus); // Output: undefined
```

## 5. Null
`null` is explicitly assigned to represent an empty or unknown value.

```js
let selectedOption = null; // No option has been selected
```

## 6. BigInt
Used for numbers larger than those that can be safely represented by the Number type.

```js
let largeNumber = 123456789012345678901234567890n; // The 'n' suffix denotes a BigInt
console.log(largeNumber);
```

## Checking Variable Types with `typeof`
The `typeof` operator is used to determine the type of a variable.

```js
let quantity = 100;
let productName = "Laptop";
let isAvailable = true;

console.log(typeof quantity); // "number"
console.log(typeof productName); // "string"
console.log(typeof isAvailable); // "boolean"
```

Understanding these basic data types allows you to effectively manage and manipulate values in JavaScript.
