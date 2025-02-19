# Callbacks

### Imagine building a web application and need to fetch user data from a database.
```js
function fetchData() {
    let data = { username: "John Doe", role: "Admin" };
    return data;
}

function showData(data) {
    console.log(`Username is ${data.username} and role is ${data.role}`);
}

const userData = fetchData();
showData(userData);
```
```js
fetchData() // retrieves user data and returns it immediately.

showData(userData) //then logs the user's details.
```

### Imagine now fetchData() is modified to simulate an API request using setTimeout:
```js
function fetchData() {
  setTimeout(() => {
    let data = { username: "John Doe", role: "Admin" };
    return data;
  }, 2000);
}

function showData(data) {
  console.log(`Username is ${data.username} and role is ${data.role}`);
}

const userData = fetchData();
showData(userData);
setTimeout()// delays execution of the function, making it asynchronous.
```
```js
fetchData() //does not wait for the data to be ready—it returns undefined immediately.
```
```js
undefined
```
### When showData(userData) runs, userData is undefined, leading to errors.

- ### We therefore use callbacks

### A `callback` function is passed as an argument to another function, ensuring that execution happens only after the asynchronous operation is complete.
```js
function fetchData(callback) {
  setTimeout(() => {
    let data = { username: "John Doe", role: "Admin" };
    callback(data);
  }, 2000);
}

fetchData(function (data) {
  console.log(`Username is ${data.username} and role is ${data.role}`);
});
```
### *Callback hell is a situation where too many nested callbacks make the code unreadable and hard to manage.

### Assuming we are fetching data with multiple data points

- ### Fetch user data (e.g., username and role)

- ### Fetch user's posts after getting user data

- ### Fetch comments on a post after retrieving posts

- ### Display all the data after everything is fetched.

### Now applying callbacks:
```js
function fetchUser(callback) {
  setTimeout(() => {
    console.log("Fetched user data");
    let user = { username: "John Doe", role: "Admin" };
    callback(user);
  }, 2000);
}

function fetchPosts(user, callback) {
  setTimeout(() => {
    console.log(`Fetched posts for ${user.username}`);
    let posts = ["Post 1", "Post 2", "Post 3"];
    callback(posts);
  }, 2000);
}

function fetchComments(post, callback) {
  setTimeout(() => {
    console.log(`Fetched comments for ${post}`);
    let comments = ["Nice post!", "Great work!", "Interesting read"];
    callback(comments);
  }, 2000);
}

// Callback Hell (Nested Callbacks)
fetchUser((user) => {
  fetchPosts(user, (posts) => {
    fetchComments(posts[0], (comments) => {
      console.log(`User: ${user.username}, Role: ${user.role}`);
      console.log(`Posts: ${posts}`);
      console.log(`Comments on first post: ${comments}`);
    });
  });
});
```
### This raise the following problems: 
- ### The indentation keeps increasing.
- ### Difficult debugging.
- ### If we add more steps the nesting increases further.

### We therefore replace callbacks with Promises to avoid *callback hell.

