# JavaScript Control Statements Tutorial: Assignment 4

## Introduction

JavaScript is a powerful scripting language used primarily for web development. This guide will provide an introduction to some of the fundamental control statements in JavaScript, including if/else, switch, and logical operators.

## Table of Contents

- Boolean Values in JavaScript
- Types of Conditional Statements
- Code Block Delimiters
- Short-Circuit Evaluation
- The "Dangling Else" Problem
- Switch or Case Statements

## Boolean Values in JavaScript

In JavaScript, the boolean values are true and false.

## Types of Conditional Statements

JavaScript provides the following conditional statements:

**if/else:**
One-condition if/else:

```javascript
if (x === true) {
    console.log("x is true");
} else {
    console.log("x is not true");
}
```

**Multi-condition if/else:**

```javascript
if (x > 0 && y < 10) {
    console.log("Condition met");
} else {
    console.log("Condition not met");
}
```
 **if/else if/else:** 

```javascript
if (x > 10) {
    console.log("x is greater than 10");
} else if (x > 5) {
    console.log("x is greater than 5 but less than or equal to 10");
} else {
    console.log("x is less than or equal to 5");
}
```
JavaScript primarily uses if/else for conditional statements, but it doesn't have an "unless" statement like Perl.

## Code Block Delimiters

JavaScript delimits code blocks using curly braces {}.

## Short-Circuit Evaluation

JavaScript uses short-circuit evaluation. When evaluating an AND (&&) expression, if the first condition is false, JavaScript won't check the second condition.

```javascript
let x = false;
let y = true;

if (x && y) { 
    // This block won't run, because x is false, so y is not even checked
}
```
## The "Dangling Else" Problem

In cases of nested if-else statements, the "else" binds to the nearest "if" in JavaScript. For example:


```javascript
if (x > 0)
    if (y > 0)
        console.log("Both x and y are positive");
    else
        console.log("x is negative or zero");
```

In the above code, the else binds to the inner if.

## Switch or Case Statements

JavaScript has a switch statement. Each case in a switch should be ended with a break unless you want to allow cases to cascade.

```javascript
switch (value) {
    case 1:
        console.log("One");
        break;
    case 2:
        console.log("Two");
        break;
    default:
        console.log("Other value");
}
```
In JavaScript, without a break, multiple cases will execute.

## Conclusion

Understanding control statements in JavaScript is fundamental for decision-making in your code. Practice the above examples and experiment with variations to strengthen your grasp of these concepts.

## Sources
[Mozilla Developer Network - JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
