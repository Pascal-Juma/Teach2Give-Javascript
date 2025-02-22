# Event Propagation

### Is how events flow through the DOM tree.
### It also defines the element order.

- ### Bubbling and capturing, are two ways of even propagation in the HTML DOM.

### In bubbling, the innermost element's event is handled first and then the outer. 

### In capturing, the outermost element's event is handled first and then the inner.
### With the `addEventListener` method, you can specify the propagation type by passing `useCapture` (true or false). False is the default.
### For Example
```html
<div class="one">
    <div class="two">
        <div class="three">
        </div>
    </div>
</div> 
``` 
```js
const divs = document.querrySelectorAll('div');

    function logText(e){
        console.log(this.classList.value);
    }
    divs.foreach(div => div.addEventListener("Click", logText));
```
### output
```js
three
two
one
```
