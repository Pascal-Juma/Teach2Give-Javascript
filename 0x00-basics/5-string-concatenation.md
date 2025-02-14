# String Concatenation

Combining strings or what we call concatenation is the process of merging two or more strings together.

JavaScript offers several methods to combine strings.

## 1. Using the `+` Operator

The `+` operator can be used to merge strings.

```js
let firstName = "Alice";
let lastName = "Smith";
let fullName = firstName + " " + lastName;
console.log("The full name is " + fullName);
```

## 2. Using Template Literals

Template literals, introduced in ES6, use backticks (\`) and placeholders (\`${}\`) for variables.

```js
let firstName = "Alice";
let lastName = "Smith";
console.log(`The name is ${firstName} ${lastName}`);
```

## 3. Using the `+=` Operator to Append to an Existing String

The `+=` operator can be used to append a string to an existing string.

```js
let greeting = "Hi ";
greeting += "Bob.";
console.log(greeting);
```
