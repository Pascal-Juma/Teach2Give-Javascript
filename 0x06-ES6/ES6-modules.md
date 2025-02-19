# ES6 Modules

### Modular system makes it easier to manage and reuse code.

<h2> ⚠ Important Note:</h2>

### If using ES6 Modules in a browser,  add `type="module"` in the `<script>` tag, for example:
```html
<script type="module" src="main.js"></script>
```
### To use ES6 modules in Node.js:
```json
Add "type": "module" in package.json.
```

### Use .mjs file extensions.

## Exporting and Importing in ES6 Modules

### 1. Named Exports

### File: mathUtils.mjs
```js
export function add(a, b){
    return a + b;
}

export function subtract(a, b){
    return a - b;
}

export function multiply(a, b){
    return a * b;
}
```
### File: index.mjs
```js
import {
    add, subtract, multiply} from "./mathUtils.mjs";
    console.log(add(5,4));
    console.log(subtract(5,4));
    console.log(multiply(5, 4));
```

- ### Precede file name ./ when importing

### 2. Using aliases for imports
```js
import{ add as sum, subtract as difference, multiply } from "./mathUtils.mjs";
console.log(sum(5,4));
console.log(difference(5,4));
console.log(multiply(5,4));
```
### 3. Importing everything (`*` as an object)
```js
import * MathUtils from "./mathUtils.mjs";
console.log(MathUtils.add(5,4));
console.log(MathUtils.subtract(5,4));
console.log(MathUtils.multiply(5,4));
```
### 4. Default Exports

### File: logger.mjs
```js
export default function log(message) {
  console.log(`Log: ${message}`);
}
```
- ### Default exports don't need curly braces {} when importing.

### You can import a default export with any name.

### File: index.mjs
```js
import log from "./logger.mjs";

log("Hello, World");
```