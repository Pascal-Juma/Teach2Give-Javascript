# JavaScript Loops

<p>Loops in Js are very helpful if you want to run the same code repeatedly.</p>

## Different Kinds of Loops

### 1. For Loop
The `for` loop has the following syntax:

```javascript
for (initialization; condition; increment) {
    // code block to be executed
}
```
For Example

```javascript
for (let i = 0; i < 5; i++) {
    console.log("The number is " + i);
}
```

```
`i` is initialized to 0, runs while `i` is less than 5, and increments `i` by 1 on each iteration.
``` 
The output will be: 

```js
The number is 0
The number is 1
The number is 2
The number is 3
The number is 4
```

### 2. While Loop
The `while` loop has the following syntax:

```javascript
while (condition) {
    // code block to be executed
}
```
For Example

```javascript
let num = 1;

while (num <= 5) {
    console.log("Number ", num);
    num++;
}
```

`num` is initialized to 1, runs while `num` is less than or equal to 5, and increments `num` by 1 on each iteration.

The output will be:
```js
Number  1
Number  2
Number  3
Number  4   
Number  5
```


### 3. Do While Loop
The `do...while` loop has the following syntax:

```javascript
do {
    // code block to be executed
} while (condition);
```
For Example

```javascript
let x = 1;

do {
    console.log("x ", x);
    x++;
} while (x <= 5);
```

`x` is initialized to 1, the code block runs once before checking the condition, and then continues to run while `x` is less than or equal to 5, incrementing `x` by 1 on each iteration.

The output will be:
```js
x  1
x  2
x  3
x  4
x  5
```
### 4. Break Statement
The `break` statement terminates the loop when a specific condition is met.

For Example:

```javascript
for (let i = 0; i < 10; i++) {
    if (i == 5) {
        break;
    }
    console.log(i);
}
```

In this example, the loop will terminate when `i` equals 5. The output will be:

```js
0
1
2
3
4
```

### 5. Continue Statement
The `continue` statement skips the current iteration of the loop and move on to the next iteration.

For Example:

```javascript
for (let i = 0; i < 10; i++) {
    if (i == 5) {
        continue;
    }
    console.log(i);
}
```

In the loop will skip the iteration when `i` equals 5. 

The output will be:

```js
0
1
2
3
4
6
7
8
9
```