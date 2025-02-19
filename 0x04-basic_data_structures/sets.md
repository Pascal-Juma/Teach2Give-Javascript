# Sets

- ### A set represents a collection of unique values.

## Properties of a Set

1. ### Unique elements
1. ### No indexing 
1. ### No order 

## Creating a Set

```javascript
const mySet = new Set([1, 2, "a", "John"]);
console.log(mySet);
```

## Set Methods

### 1. `add(value)`

```javascript
const mySet = new Set();
mySet.add("John");
mySet.add(44);
mySet.add(44); //output -> Duplicate, will not be added
mySet.add("Doe");
mySet.add(true);
mySet.add(true); // Duplicate, will not be added
mySet.add(false);
console.log(mySet); // Set(5) { 'John', 44, 'Doe', true, false }
```

### 2. `delete(value)`

```javascript
const mySet = new Set(["John", 44, "Doe", true, false]);
mySet.delete("John");
mySet.delete(true);
mySet.delete(44);
console.log(mySet); // output -> Set(2) { 'Doe', false }
```

### 3. `has(value)`

```javascript
const mySet = new Set(["John", 44, "Doe", true, false]);
console.log(mySet.has("John")); //output -> true
console.log(mySet.has("June")); // output -> false
```

### 4.`size`

```javascript
const mySet = new Set(["John", 44, "Doe", true, false]);
console.log(mySet.size); // output -> 5
```