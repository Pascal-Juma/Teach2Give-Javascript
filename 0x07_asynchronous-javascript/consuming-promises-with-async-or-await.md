# Consuming Promises With Async/Await
- ### They make asynchronous code looks like synchronous one.

- ### `async/await` mostly consumes promises.
```js
function fetchUser(){
    return new Promise(function (resolve, reject){
        let error = true;
        if(error === true){
            reject("There was an error");
        }else{
            resolve({ username: "_john", role: "Admin" });
        }
    });
}
async function processUser(){
    const user = await fetchUser();
    console.log(user);
}

processUser();
```
## Handling Errors 

```js
function fetchUser(){
    return new Promise(function(resolve, reject){
        let error = true;
        if(error === true){
            reject("There was an error");
        }else{
            resolve({ username: "_john", role: "Admin" });
        }
    });
}

async function processUser(){
    try{
        const user = await fetchuser();
        console.log(user);
    }catch{
        console.log("Err");
    }
}

processUser();
```

### The catch block can also receive the error thrown from the promise:
```js
function fetchUser(){
    return new Promise(function(resolve, reject){
        let error = true;
        if(error === true){
            reject("There was an error");
        }else{
            resolve({username: "_john", role: "Admin"});
        }
    });
}

async function processUser(){
    try{
        const user = await fecthUser();
        console.log(user);
    }catch(error){
        console.log(error);
    }
}

processUser();
```
### `try..catch` also has a `finally` block:\

