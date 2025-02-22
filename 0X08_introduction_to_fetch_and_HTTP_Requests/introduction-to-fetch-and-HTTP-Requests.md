# Introduction to `fetch` and HTTP Requests

- ### `fetch` function allows your code to communicate with other computers  over the internet.

## HTTP Request
- ### HTTP (HyperText Transfer Protocol) is how computers communicate over the web.

### They include:

- ### GET: *a computer asks for data.*

- ### POST: *a computer sends data to be created on the server.*

- ### PUT: *a computer requests for data updates* 

- ### DELETE: *a computer requests for data to be deleted.*
### Most websites send and receive data using HTTP requests.

## Making a simple fetch request
### Let's make a simple fetch request to get data from a public API.
```js
fetch("https://jsonplaceholder.typicode.com/users")
.then(function (response) {
    return response.json();
})
.then(function (data){
    console.log(data);
})
.catch(function (error){
    console.log("There was was an error");
    console.log(error);
});
```
### Explanation:

### `fetch("https://jsonplaceholder.typicode.com/users/1")` Asks the server for user data.
```js
.then(function (response){
    return response.json();
})
```
- ### We convert the response to JSON to make it readable to the computer.
```js
.then(function (data) {
    console.log(data);
  })
```
- ### Receives data from the previous step and displays it in the user's console.
```js
.catch(function (error) {
    console.log("There was an error");
    console.log(error);
  })
```
- ### This shows an error, if something goes wrong.

## Using async await for easier syntax
```js
async function fetchUser(){
    try{
        const response = await fetch("https://jsonplaceholder.typecode.com/users/1",);
    const data = await response.json(); // Convert response to JSON
    console.log(data); // Display user data
    }catch (error){
        console.error("Error:", error); // Handle errors
    }
}

fetchUser();
```
## Handling Errors
You should always handle errors, if  something goes wrong.
```js
async function fetchUser(){
    try{
        const response = await fetch("https://jsonplaceholder.typecode.com/users/1",);
        if (!response.ok){
            console.log("something went wrong");
            return;
        }
        const data = await response.json(); // Convert response to JSON
        console.log(data); // Display user data
    }catch(error){
        console.error("Error:", error); // Handle errors
    }
}

fetchUser();
```