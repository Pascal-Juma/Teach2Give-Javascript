## JavaScript Conditionals

## Conditional Statements

 #### Frequently, when writing code, you need to execute different actions based on various conditions.

<p>Conditional statements help us achieve this.</p>
<ul>
    <li>Use <code>if</code> to specify a block of code to be executed, if a specified condition is true</li>
    <li>Use <code>else</code> to specify a block of code to be executed, if the same condition is false</li>
    <li>Use <code>else if</code> to specify a new condition to test, if the first condition is false</li>
    <li>Use <code>switch</code> to specify many alternative blocks of code to be executed</li>
</ul>

### 1. The `if` Statement

#### Syntax
```javascript
if (condition) {
    // block of code to be executed if the condition is true
}
```
####  For Example
Grade a "Distinction" grade if the score is greater than or equal to 70:

```javascript
if (score >= 70) {
    grade = "Distinction";
}
```

The program will execute true if we declare a value like 80 otherwise it will not

### 2. The `else` Statement

#### Syntax
```javascript
if (condition) {
    // block of code to be executed if the condition is true
} else {
    // block of code to be executed if the condition is false
}
```
#### For Example
Grade a "Fail" grade if the score is less than 70:

```javascript
if (score >= 70) {
    grade = "Distinction";
} else {
    grade = "Fail";
}
```


The program will execute the else block if the score is less than 70, for example, 65.

### 3. The `else if` Statement

#### Syntax
```javascript
if (condition1) {
    // block of code to be executed if condition1 is true
} else if (condition2) {
    // block of code to be executed if condition1 is false and condition2 is true
} else {
    // block of code to be executed if both condition1 and condition2 are false
}
```
#### For Example
Grade a "Pass" grade if the score is between 50 and 69, and a "Fail" grade if the score is less than 50:

```javascript
if (score >= 70) {
    grade = "Distinction";
} else if (score >= 50) {
    grade = "Pass";
} else {
    grade = "Fail";
}
```

The program will execute the else if block if the score is between 50 and 69, for example, 55.

### 4. The `switch` Statement

#### Syntax
```javascript
switch(expression) {
    case x:
        // code block
        break;
    case y:
        // code block
        break;
    default:
        // code block
}
```
#### For Example
Assign a grade based on the score using a switch statement:

```javascript
switch(true) {
    case (score >= 70):
        grade = "Distinction";
        break;
    case (score >= 50):
        grade = "Pass";
        break;
    default:
        grade = "Fail";
}
```
The program will execute the appropriate case block based on the score, for example, if the score is 75, it will assign "Distinction".
