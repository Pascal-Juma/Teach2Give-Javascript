# JavaScript Operators

Operators in JavaScript are symbols that perform operations on values, known as operands.

They are essential for performing calculations, comparisons, and logical operations.

JavaScript operators are categorized as follows:

## 1. Arithmetic Operators

These operators are used for mathematical calculations.

### a. Addition (+)

Adds two numbers:

```js
let d = 4;
let p = 7;
console.log(d + p); // 11
```

Also used for string concatenation:

```js
let firstName = "John";
let lastName = "Doe";
console.log(firstName + lastName); // JohnDoe
```

### b. Subtraction (-)

Subtracts the right operand from the left:

```js
let d = 10;
let p = 5;
console.log(d - p); // 5
```

### c. Multiplication (*)

Multiplies two numbers:

```js
let d = 10;
let p = 5;
console.log(d * p); // 50
```

### d. Division (/)

Divides the left operand by the right:

```js
let d = 10;
let p = 5;
console.log(d / p); // 2
```

### e. Modulus (%)

Returns the remainder of the division:

```js
let d = 10;
let p = 5;
console.log(d % p); // 0
```

### f. Exponentiation (**)

Raises the left operand to the power of the right:

```js
let d = 10;
let p = 5;
console.log(d ** p); // 100000
```

### g. Decrement Operator

Decreases a variable's value by 1.

- Post-decrement `(d--)`: returns the original value, then decrements.
- Pre-decrement `(--d)`: decrements first, then returns the updated value.

### h. Increment Operator

Increases a variable's value by 1.

- Post-increment `(d++)`: returns the original value, then increments.
- Pre-increment `(++d)`: increments first, then returns the updated value.

```js
let x = 5;
console.log(x++); // 5
console.log(x); // 6

let y = 5;
console.log(++y); // 6
```

## 2. Assignment Operators

Used to assign values to variables.

### a. Simple Assignment (=)

Assigns a value to a variable:

```js
let x = 5;
```


### b. Subtraction Assignment (-=)

Subtracts a value from a variable:

```js
let x = 6;
x -= 2; // x = x - 2 → 4
```

### c. Addition Assignment (+=)

Adds a value to a variable:

```js
let x = 4;
x += 7; // x = x + 7 → 11
```

### d. Division Assignment (/=)

Divides a variable:

```js
let x = 6;
x /= 3; // x = x / 3 → 2
```

### e. Multiplication Assignment (*=)

Multiplies a variable:

```js
let x = 7;
x *= 4; // x = x * 4 → 28
```

## 3. Comparison Operators

Used to compare values, returning true or false.

### a. Equality (==)

Returns true if the operands are equal:

```js
let d = 10;
let p = 5;
console.log(d == p); // false
console.log(d == 10); // true
```

Note: Ignores data type:

```js
console.log(10 == "10"); // true
```

### b. Strict Equality (===)

Returns true if the operands are equal and of the same type:

```js
let d = 10;
let p = 5;
console.log(d === p); // false
console.log(d === 10); // true
```

Note: Considers data type:

```js
console.log(10 === "10"); // false
```

### c. Inequality (!=)

Returns true if the operands are not equal:

```js
let d = 10;
let p = 5;
console.log(d != p); // true
console.log(d != 10); // false
```

Note: Ignores data type:

```js
console.log(10 != "10"); // false
```

### d. Strict Inequality (!==)

Returns true if the operands are not equal or not of the same type:

```js
let d = 10;
let p = 5;
console.log(d !== p); // true
console.log(d !== 10); // false
```

Note: Considers data type:

```js
console.log(10 !== "10"); // true
```

### e. Greater Than (>)

Returns true if the left operand is greater than the right:

```js
let d = 10;
let p = 5;
console.log(d > p); // true
console.log(p > d); // false
```

### f. Less Than (<)

Returns true if the left operand is less than the right:

```js
let d = 10;
let p = 5;
console.log(d < p); // false
console.log(p < d); // true
```

### g. Greater Than or Equal To (>=)

Returns true if the left operand is greater than or equal to the right:

```js
let d = 10;
let p = 5;
console.log(d >= p); // true
console.log(p >= d); // false
console.log(10 >= 10); // true
```

### h. Less Than or Equal To (<=)

Returns true if the left operand is less than or equal to the right:

```js
let d = 10;
let p = 5;
console.log(d <= p); // false
console.log(p <= d); // true
console.log(10 <= 10); // true
```

## 4. Logical Operators

Used for boolean logic.

### a. AND (&&)

Returns true only if both operands are true:

```js
console.log(true && true); // true
console.log(true && false); // false
```

### Truth Table for AND

| Expression 1 | Expression 2 | Result |
|--------------|---------------|--------|
| true         | true          | true   |
| true         | false         | false  |
| false        | true          | false  |
| false        | false         | false  |

### b. NOT (!)

Negates the boolean value of an expression:

```js
console.log(!true); // false
console.log(!false); // true
```

### c. OR (||)

Returns true if at least one of the operands is true:

```js
console.log(true || false); // true
console.log(false || false); // false
```

### Truth Table for OR

| Expression 1 | Expression 2 | Result |
|--------------|---------------|--------|
| true         | true          | true   |
| true         | false         | true   |
| false        | true          | true   |
| false        | false         | false  |

