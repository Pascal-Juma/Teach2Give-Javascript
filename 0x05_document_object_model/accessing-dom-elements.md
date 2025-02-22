<h1>Accessing/Finding Dom Elements</h1>

### We first start by accessing the document object in a html page.

## Methods for accessing DOM elements
###  1. `document.getElementById(elementId)`
```html
<button id="my-button">Click Me</button>
```
```js
const button = document.getElementById("my-button");
console.log(button); // <button id="my-button">Click Me</button>
```
 ### 2. `document.getElementsByTagName(name)`
### e.g finding all paragraph elements in a page.
```html
<p>Hello, World</p>
<p>JavaScript is awesome</p>
<p>JavaScript is great</p>
```
```js
const paragraphs = document.getElementsByTagName("p");
console.log(paragraphs); // [p, p, p]
```
 ### 3. `document.getElementsByClassName(className)`
```html
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```
```js
const texts = document.getElementsByClassName("text");
console.log(texts); // [p.text, p.text]
```
### 4. `document.querySelector(selector)`
### Selects the first element that matches a specified CSS selector, id or tag name.
```html
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```
 ### javascript
 ```js
const firstText = document.querySelector(".text");
console.log(firstText);
```
### 5. `document.querySelectorAll(selector)`
### Selects all elements in the document 
```html
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```
```js
const paragraphs = document.querySelectorAll('p');
console.log(paragraphs); // [p.text, p.text, p]
```