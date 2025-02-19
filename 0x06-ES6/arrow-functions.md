# Arrow functions

### Arrow functions (`=>`) provides a more concise syntax for writing functions.

### They remove the `function` keyword.
### Before
```js
function add(a, b) {
  return a + b;
}

console.log(add(4, 12));
```
### After
```js
const add = (a, b) => a + b;
 
console.log(add(4, 12));
```
### However, (`=>`) don't have their own `this` keyword.

### They excel in scenarios such as:
- ### call back 
- ### array methods
- ### event listeners
- ### code simplification(function)
