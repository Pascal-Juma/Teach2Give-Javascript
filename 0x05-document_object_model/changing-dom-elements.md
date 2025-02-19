# Changing DOM Elements

## A. Changing the content of HTML elements
### 1. `innerHTML`

- ### Sets or gets the HTML content of an element.
```html
<div id="my-div">
    <h1>Hello, world</h1>
    <p>JavaScript is awesome</p>
</div>
```
### JavaScript
```js
const div = document.getElementById("my-div");
console.log(div.innerHTML);
div.innerHTML = `<h1>New content</h1>`;
console.log(div.innerHTML);
```
### 2. `innerText`
- ### Sets or get the text content of an element.
```html
<div id="my-div">
    <h1>Hello, world</h1>
    <p>JavaScript is awesome</p>
</div>
```
```js 
const div = document.getElementById("my-div");
console.log(div.innerText);
div.innerText = "New content";
console.log(div.innerText);
```

### 3. `textContent`
- ### Sets or gets the text content of an element and its descendants.
```html
<div id="my-div">
    <h1>Hello, world</h1>
    <p>JavaScript is awesome</p>
</div>
```
```js
const div = document.getElementById("my-div");
console.log(div.textContent);
div.textContent = "New content";
console.log(div.textContent);
```
## B. Changing the attribute of HTML elements
- ### We use `element.attribute = value`.
```html
<h1 class="title" id="title">Hello, world</h1>
```
```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.id = "awesome-title";
console.log(title); // <h1 class="title" id="awesome-title">Hello, world</h1>
```
- ### `We can also use element.setAttribute("attribute", "value")`
```html
<h1 class="title" id="title">Hello, world</h1>
```
```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.setAttribute("id", "awesome-title");
console.log(title);
```
## C. Changing the styling of HTML elements﻿
- ### We use `element.style.property = "value"`.
```js
const title = document.getElementById("title");
title.style.border = "3px solid red";
title.style.fontSize = "48px";
title.style.borderRadius = "5px";
```