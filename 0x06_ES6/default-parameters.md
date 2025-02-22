# Default Parameters

### They allow you to set a default value for function parameters if no argument is passed.
```js
function greet(name = "Guest"){
    console.log(`Hello ${name}`);
}
greet(); //Hello Guest
greet("John Doe"); // Hello John Doe
```
### In this example:

### If no argument is provided -> "Guest".

### If an argument is provided, it overrides the default value.