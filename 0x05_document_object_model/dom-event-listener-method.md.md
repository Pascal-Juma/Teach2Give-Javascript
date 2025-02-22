# DOM Event Listener Method

### The `addEventListener()` method attaches an event handler to a specified element.

### The first parameter is the type of event e.g click

### The second is the function we want to call.

### Example:
```js
const btn = document.getElementById("btn");
btn.addEventListener("click", function (){
    console.log("Button Clicked");
});
```