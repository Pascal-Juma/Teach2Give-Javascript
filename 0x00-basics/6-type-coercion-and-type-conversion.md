# Type Coercion and Type Conversion

In JavaScript, type **coercion** and type **conversion** both refer to the process of changing a value from one data type to another. However, they differ in their approach and execution.

## Type Coercion (Implicit Conversion)

Happens automatically when JavaScript mixes different data types.

Common in comparisons `(==)`, string concatenation `(+)`, and math operations.

Can lead to unexpected results.

**Examples:**

```js
console.log(10 + "20"); // "1020" (Number coerced into a string)
console.log("10" - 5); // 5 (String coerced into a number)
console.log(true + 2); // 3 (true coerced into 1)
console.log(false + "15"); // "false15" (false coerced into string)
```

## Type Conversion (Explicit Conversion)

Occurs when you manually convert the data type of a value.

### Methods of Explicit Conversion

- Convert to string using `String()` or `toString()`.

```js
console.log(String(123));
console.log((123).toString());
```

- Convert to number using `Number()`, `parseInt()`, or `parseFloat()`.

```js
console.log(Number("123"));
console.log(parseInt("123"));
console.log(parseFloat("123.45"));
console.log(parseInt("50px"));
```

- Convert to boolean using `Boolean()`.

**Falsy values:** 0, "", null, undefined, NaN, false.  
**Truthy values:** everything else.

```js
console.log(Boolean(0)); // false
console.log(Boolean("world")); // true
console.log(Boolean(undefined)); // false
```