# Promises
### There is:
- ### Producing code: *is code that will take some time to complete.*

- ### Consuming code: *code that must wait for results from producing code*

### A **promise**  links producing and consuming code.

### A promise has three states:

- ### Pending
- ### Fulfilled
- ### Rejection

## Creating a promise

- ### The executor function takes two parameters: resolve and  reject
### Eg.
```js
let myPromise = new Promise(function(resolve, reject){
    let x = 1;
    if(x === 1){
        resolve("x is 1");
    }else{
        eject("x is not 1");
    }
});
```
## Consuming a promise
### We use `.then()` to handle resolved value and `.catch()` to handle errors.
```js
let myPromise = new Promise(function(resolve, reject){
    let x = 5;
    if(x === 1){
        resolve("x is 1");
    }else{
        reject("x is not 1");
    }
});

myPromise
    .then((result) => {
        console.log(result);
    })
    .catch((error) => {
        console.log(error);
    });
```
## Returning a promise from a function
### Eg.
```js
function fetchUser(){
    return new Promise(function(resolve, reject){
        let error = false;
        if(error === true){
            reject("There was an error");
        }else{
            resolve({username: "_john", role: "Admin"});
        }
    });
}
fetchUser()
    .then((user) => {console.log(`Username: ${user.username}, Role: ${user.role}`);
    })
    .catch((error) => {
    console.log(error);
    });
```