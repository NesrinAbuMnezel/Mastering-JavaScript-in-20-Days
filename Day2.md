
# Day 2: 
## Values & Data Types
* **Values**
  - chunks of information we want to work with
  - that information (data) can be of different types
* **typeof**
  - tells you the type of a value
* **JS has two kinds of data:**
  - Primitive types (e.g. strings, numbers)
  - Objects (e.g. document & friends)
* **Primitive data types**
  - string
  - number
  - boolean
  - undefined
  - null
## Operators
Document Object Model it's a built in object in JS that represents the whole document.
### Finding Elements in a Web Page:
- `document.title` : the page (document) title
- `document.body` : the body element
- `document.body.children` : all the elements within the body
- `document.getElementById("board")` or `document.querySelector("#board")` : the (first) element with id="board"
- `document.getElementsByTagName("h1")` or `document.querySelectorAll("h1")` : all the h1 elements
- `document.getElementsByClassName("player")` or `document.querySelectorAll(".player")` : all the elements with class="player"
- `document.getElementsByClassName("player").length`or `document.querySelectorAll(".player").length` : the number of elements with class="player"
- `document.getElementById("p1-name").textContent` : the text inside the element with id="p1-name"
 ## Expressions
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
**Type commands in the console to retrieve**
  1. all the `p` elements <br>
    `document.getElementsByTagName("p")`
  2. the text **X** <br>
    `document.getElementById("p1-symbol").textContent`
  3. the number of sequares in the board <br>
     `document.querySelectorAll(".square").length`
  4. the text **A game you know**  <br>
     `document.querySelector("h2").textContent`
  5. change the player names to you & nighbor  <br>
     `document.querySelector("#p1-name").textContent = nesrin`
     `document.querySelector("#p2-name").textContent = ahmed`
  6. swap the player symbols  <br>
     `document.getElementById("p1-symbol").textContent = "O"`
     `document.getElementById("p2-symbol").textContent = "X"`
  7. change subtitle to **A game you know and love**  <br>
     `document.querySelector("header h2").append("  and love")`



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

### QUESTION #1

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

What will be the output of each console.log statement? **_You MUST explain WHY_**.

#### My Solution
```
true  // compare the value
false // compare the value and data type
true  // the first ! convert string to boolean the second one ! invert the false to true
```

-------------------------------------------------------------------

### QUESTION #2:


Consider the following JavaScript expression:

```javascript
console.log(4 + 5 * "7");
```

What will be the output of this expression? **_You MUST explain the steps of evaluation taken by JS_**.

#### My Solution
```
39 // here the priority for multiplication, so 5 * "7" , JS trying to convert to "7" to number (Implicit Conversion) ,which give 35
then 35 plus 4 
```

-------------------------------------------------------------------

### QUESTION #3:

Evaluate the following expression:

```javascript
let result = 5 + 2 * 3 - 1;
```

What will be the output of this expression? **_You MUST explain the steps of evaluation taken by JS_**.

#### My Solution
```
10 // here the priority for multiplication, 5 + 6 - 1 we start from left to right
```

-------------------------------------------------------------------

### QUESTION #4:

Consider the following code:

```javascript
let x = 10;
let y = '10';
console.log(x == y);
console.log(x === y);
```
What will be the output of each `console.log` statement? **_You MUST explain WHY_**.

#### My Solution
```
true  // compare the value
false // compare the value and data type
```

-------------------------------------------------------------------

### QUESTION #5:

Given the code below:

```javascript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result);
```

What is the value of result? **_You MUST explain the steps of evaluation taken by JS_**

#### My Solution
```
true  // num > 10 (Implicit Conversion) so it gives true && true || false 
```
