# Static Methods and Properties

### Static methods and static properties belong to a class itself rather than its instances.

## Static Methods
### A static method is defined using the `static` keyword inside a class.
```js
class MathUtils{
    static add(a, b){
        return a + b;
    }

    static subtract(a, b){
        return a - b;
    }
}

// Calling static methods directly from the class
console.log(MathUtils.add(10, 5)); // 15
console.log(MathUtils.subtract(10, 5)); // 5
```
### Trying to call a static method on an instance:
```js
const math = new MathUtils();
console.log(math.add(10, 5)); //Error: math.add is not a function
```
## Static Property
### A static property is a variable that belongs to the class.
```js
class Counter{
    static count = 0; //static property

    static increment(){
        counter.count++; // Assessing the static property
    }

    static getCount(){
        return Counter.count;
    }
}

// Assessing static property without an instance
console.log(Counter.getCount()); // 0

Counter.increment();
Counter.increment();

console.log(Counter.getCount()); // 2
```