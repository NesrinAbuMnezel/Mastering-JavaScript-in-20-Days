
# Day 2: Hoisting

This README file summarizes the JavaScript lesson on hoisting. Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their scope during the compilation phase.

## Lesson Summary

In this lesson, we explored hoisting in JavaScript. Here are the key points covered:

- Hoisting is the process of moving variable and function declarations to the top of their scope.
- Variable declarations are hoisted but not their assignments. They are accessible but have an initial value of `undefined`.
- Function declarations are also hoisted, allowing them to be called before they are defined.
- Hoisting does not apply to function expressions, arrow functions, or variables declared with `let` or `const`.

## Coding Examples

```javascript
// Example 1: Variable Hoisting
console.log(x); // Output: undefined
var x = 10;
console.log(x); // Output: 10

// Example 2: Function Hoisting
hoistedFunction(); // Output: "Hello, World!"

function hoistedFunction() {
  console.log("Hello, World!");
}

```


## Coding Exercises

###  QUESTION #1
Consider the following JavaScript code:
```javascript
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b);
console.log(b === c);
console.log(!!d);
```
What will be the output of each console.log statement? You MUST explain WHY.


#### My Solution

###  QUESTION #2
Consider the following JavaScript code:
```javascript
console.log(4 + 5 * "7");
```
What will be the output of each console.log statement? You MUST explain WHY.


#### My Solution
###  QUESTION #3
Consider the following JavaScript code:
```javascript
let result = 5 + 2 * 3 - 1;
```
What will be the output of each console.log statement? You MUST explain WHY.


#### My Solution
###  QUESTION #4
Consider the following JavaScript code:
```javascript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result);
```
What will be the output of each console.log statement? You MUST explain WHY.


#### My Solution
###  QUESTION #5
Consider the following JavaScript code:
```javascript
console.log(4 + 5 * "7");
```
What will be the output of each console.log statement? You MUST explain WHY.


#### My Solution







