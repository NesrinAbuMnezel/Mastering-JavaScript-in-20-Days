
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
## DOM 
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
  






### Coding Examples

```javascript

<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <title>JavaScripTacToe</title>
  </head>
  <body>
    <header>
    <h1>Tic Tac Toe</h1>
    <h2>A game you know</h2>
    <div id="players">
        <p id="p1" class="player">Player <span id="p1-symbol">X</span>: <span id="p1-name">Anjana</span></p>
        <p id="p2" class="player">Player <span id="p2-symbol">O</span>: <span id="p2-name">Marc</span></p>
    </div>
    </header>
    <div id="board">
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
    </div>
  </body>
</html>


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
