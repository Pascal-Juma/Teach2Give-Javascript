# JavaScript Objects

- ### an object is a collection of key-value pairs.
- ### A method is function inside an object.

## Creating Objects
### 1. Using Object Literal
- ### We use curly braces.
```js
const student = {           //<-----
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};                          //<-----
```
### 2. Using `new Object()`
## Eg
```js
const student = new Object();       //<-----
student.firstName = "John";
student.lastName = "Doe";
student.age = 25;
student.isStillStudying = true;
student.greet = function () {
  console.log("Hello, World!");
};
```
### 3. Using a Constructor Function
## Eg
```js
function Student(firstName, lastName, age, isStillStudying) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.age = age;
  this.isStillStudying = isStillStudying;
  this.greet = function () {
    console.log("Hello, World!");
  };
}
const student = new Student("John", "Doe", 25, true);
```
## Accessing Object Properties
### a. Dot notation
## Eg
```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(student.firstName); // output -> John
console.log(student.lastName); // output -> Doe
```
### b. Bracket notation
```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

console.log(student["firstName"]); //output -> John
console.log(student["lastName"]); //output -> Doe
console.log(student["age"]); // output -> 25
console.log(student["isStillStudying"]); //output -> true
```

## Modifying objects
### i. Adding new properties
- ### Using  the dot or bracket notation
```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

student.major = "Computer Science";
student["graduationYear"] = 2026;
console.log(student);
//output -> { firstName: 'John',
//output ->           lastName: 'Doe',
// output ->          age: 25,
// output ->          isStillStudying: true,
//output ->           greet: [Function: greet],
// output ->          major: 'Computer Science',
//  output ->         graduationYear: 2026 }
```
### ii. Updating a property
```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

student.age = 37;
student["isStillStudying"] = false;
```
### iii. Deleting a property
```js
const student = {
  firstName: "John",
  lastName: "Doe",
  age: 25,
  isStillStudying: true,
  greet: function () {
    console.log("Hello, World!");
  },
};

delete student.age;
delete student.isStillStudying;
``` 
### iv. Checking Properties in an Object

- ### The `in` Keyword
```js
const student = {
    firstName: "John",
    lastName: "Doe",
    age: 25,
    isStillStudying: true,
    greet: function () {
        console.log("Hello, World!");
    },
};

console.log("firstName" in student); //output -> true
console.log("middleName" in student); // output -> false
```

- ### The `hasOwnProperty()` Method
```js
const student = {
    firstName: "John",
    lastName: "Doe",
    age: 25,
    isStillStudying: true,
    greet: function () {
        console.log("Hello, World!");
    },
};

console.log(student.hasOwnProperty("firstName")); // output -> true
console.log(student.hasOwnProperty("middleName")); // output -> false
```

## Object Methods
### I. `Object.keys(objectName)`
### Eg
```js
const student = {
    firstName: "John",
    lastName: "Doe",
    age: 25,
    isStillStudying: true,
    greet: function () {
        console.log("Hello, World!");
    },
};

console.log(Object.keys(student));
//output ->  [ 'firstName', 'lastName', 'age', 'isStillStudying', 'greet' ]
```

### II. `Object.values(objectName)`
### Eg.
```js
const student = {
    firstName: "John",
    lastName: "Doe",
    age: 25,
    isStillStudying: true,
    greet: function () {
        console.log("Hello, World!");
    },
};

console.log(Object.values(student));
//output -> [ 'John', 'Doe', 25, true, [Function: greet] ]
```

### III. `Object.freeze(objectName)`
- ### It  prevents an object from modification.
```js
const student = {
    firstName: "John",
    lastName: "Doe",
    age: 25,
    isStillStudying: true,
    greet: function () {
        console.log("Hello, World!");
    },
};

Object.freeze(student);
student.middleName = "Smith"; //output -> won't work
```

## Iterating Over an Object Using the `for..in` Loop

```js
const student = {
    firstName: "John",
    lastName: "Doe",
    age: 25,
    isStillStudying: true,
    greet: function () {
        console.log("Hello, World!");
    },
};

for (let key in student) {
    console.log(key);
}
```
