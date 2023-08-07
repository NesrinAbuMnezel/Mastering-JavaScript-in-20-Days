
# Day 1: 
## Introduction 
* **What is a  JavaScript?**
  - programming language, it's a language of the web.
  - language to modify and interact with HTML.
  - dynamic programming language.
  - JS was created in 1995 by Brendan Eich in 10 days.
  - we can run JS in the browser and on servers using a project called node js.
* **Where to write  JavaScript?**
  - the browser's JS console.
  - local text file in editor, e.g. VS Code.
  - online playground e.g. CodePen, CodeSandbox. 
### Coding Examples

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

### [Compound Assignment With Augmented Multiplication](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)

#### My Solution


```javascript
let a = 5;
let b = 12;
let c = 4.6;

// Only change code below this line
a  *= 5;
b *= 3 ;
c *= 10;
```
### [Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)

#### My Solution


```javascript
let myStr="This is the first sentence. ";
myStr+="This is the second sentence.";

```
### [Use Dot Notation to Access the Properties of an Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-dot-notation-to-access-the-properties-of-an-object)

#### My Solution


```javascript
let dog = {
  name: "Spot",
  numLegs: 4
};
// Only change code below this line
console.log(dog.name);
console.log(dog.numLegs);

```
