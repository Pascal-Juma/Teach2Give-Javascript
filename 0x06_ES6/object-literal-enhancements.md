# Object Literal Enhancements
### These enhancements include:

### 1. Shorthand Property Names
### Omit the value assignment, if a variable name matches the property name.

### Before ES6:
```js
const firstName = "John";
const lastName = "Doe";
const age = 25;

const user = { firstName: firstName,
               lastName: lastName,
               age: age }; //correct
console.log(user); // { firstName: 'John', lastName: 'Doe', age: 25 }
```
### With ES6:
```js
const firstName = "John";
const lastName = "Doe";
const age = 25;

const user = { firstName, lastName, age }; // correct
console.log(user); // { firstName: 'John', lastName: 'Doe', age: 25 }
```
### 2. Method shorthand
### Before ES6:
```js
const user = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  introduction: function () {
    console.log(`My name is ${this.firstName} ${this.lastName}`);
  },
};
user.introduction();
```
### With ES6:
```js
const user = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  introduction() {
    console.log(`My name is ${this.firstName} ${this.lastName}`);
  },
};
user.introduction();
```
## Computed Property Names
### You can wrap  expressions in square brackets `[]`.
```js
const user = {
  ["first" + "Name"]: "John",
  lastName: "Doe",
  age: 25,
};
console.log(user); // { firstName: 'John', lastName: 'Doe', age: 25 }
```