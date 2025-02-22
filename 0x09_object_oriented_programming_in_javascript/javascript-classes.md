# JavaScript Classes

- ### A class is a blueprint of an object.

## Creating a class
### To create a class use the `class` keyword then the class name. Inside it, define a constructor method to initialize object properties.
```js
class User {
    constructor(name, age){{
        this.name = name;
        this.age = age;
    }
    
    greet(){
        console.log(`My name is ${this.name}`);
    }
    }
}
```
- ### The `constructor` method initializes the object's properties.

 ## Creating instances of a class

### To create an instance of a class, use the `new` keyword.
```js
class User {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`My name is ${this.name}`);
  }
}
const user1 = new User("John Doe", 25);
user1.greet(); // My name is John Doe