# Arrays in JavaScript

### An array is a collection of elements stored at contiguous memory locations.

### You can access the values by referring to an index number.

## Creating an array
### This is done by:
### 1. Using the array literal 

### Syntax:

```js
 const arrayName = ["item1", "item2","item3", "..."];
 ```
### E.g 
```js
    const students = ["John", "Ken", "June", "Jack"];
```
### 2. Using the Array() constructor
### Syntax:
```js
const arrayName = new Array("item1", "item2","item3", "...");
```
### E.g
```js 
    const students = new Array("John", "Ken", "June", "Jack");
```
### new Array() constructor nested:
```js
    const arr = new Array(1, 2, new Array(5, 6, new Array(30, 40)));
```
### However, always use array literal to create an array.

## Accessing array elements
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students[0]); //John
console.log(students[1]); //Ken
console.log(students[2]); //June
```
## Basic Array methods
### a. Length of an array(size).
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.length); //output ->  4
```
### b. pop
### The pop method removes the last item of an array.
```js
const students = ["John", "Ken", "June", "Jack"];
students.pop();
console.log(students); //output -> [ 'John', 'Ken', 'June' ]
```
### c. push
### It adds a new element at the end of the array.
```js
const students = ["John", "Ken", "June", "Jack"];
students.push("Nancy");
console.log(students); //output ->  ['John', 'Ken', 'June', 'Jack', 'Nancy']
```
### d. shift
### It removes the first item of an array.

```js
const students = ["John", "Ken", "June", "Jack"];
students.push("Nancy");
console.log(students); // output -> ['John', 'Ken', 'June', 'Jack', 'Nancy']
```
### e. unshift ()
### It adds a new element at the beginning of the array.
```js
const students = ["John", "Ken", "June", "Jack"];
students.unshift("Nancy");
console.log(students); // output -> ['Nancy', 'John', 'Ken', 'June', 'Jack']
```
### f. indexOf ()
### It returns the index of the first occurrence of the specified value.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.indexOf("June")); // output ->  2
```
### g. lastIndexOf ()
### It returns the index of the last occurrence of the specified value.

```js
const students = ["John", "Ken", "June", "Jack", "June"];
console.log(students.lastIndexOf("June")); // output -> 4
```
### h. join ()
### It combines all elements of an array into a string.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.join("   ++")); // output -> John   ++ Ken   ++ June   ++ Jack
```
### i. concat ()
### It combines two or more arrays into a single array.
```js
const arr1 = ["jack", "franklin", "june"];
const arr2 = ["andrew", "alex", "ken"];
console.log(arr1.concat(arr2));
// output ->[ 'jack', 'franklin', 'june', 'andrew', 'alex', 'ken' ]
```
### j. at()
### It returns the element at the specified index.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.at(2)); // output -> June
console.log(students.at(0)); // output -> John
```
### k. flat()
### It converts a multidimensional array to a one-dimension array.
```js
const students = [
  ["jack", "franklin"],
  ["june", "andrew"],
  ["alex", "ken"],
];
console.log(students.flat());
//output ->  ['jack', 'franklin', 'june', 'andrew', 'alex', 'ken']
```
### l. includes()
### It checks if an array includes a specified value.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.includes("Ken")); //output -> true
console.log(students.includes("Elvis")); //output -> false
```