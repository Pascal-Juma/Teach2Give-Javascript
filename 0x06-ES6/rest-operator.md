# Rest Operator(`...`)
### It collects multiple elements into a single array.

## Rest Operator Use Cases
### 1. Rest in function parameters
- ### We use it when a function has multiple parameters but we don’t know how many arguments will be passed.
### Eg. 
```js
function myFunction(...numbers) {
  console.log(numbers);
}

add(5, 6);
add(10, 14, 23, 12, 9);
add(2);
```