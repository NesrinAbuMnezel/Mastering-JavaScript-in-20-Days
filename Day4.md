
# Day 4: 
## Quiz Project Functions
* **Functions**
  - values are things
  - variables point to things
  - functions do things
  - declaring (creating) a function:
    ```javascript
    function half(x) {
    return x / 2;
    }
    ```
  - calling (using) a function:
    ```javascript
    const one = half(2);
    ```
  - Parameters & Arguments
    ```javascript
    function add(x, y) { // Parameters
    return x + y;
    }
    add(2,3);   // Arguments
    ```
 * **Arrow functions**
   - The => "fat arrow" lets us create an unnamed function without much code `(x, y) => x + y`
   - For one-parameter functions, parentheses are optional `x => x*x` => `(x) => x*x`
  
## Events & Handlers
 * **Event**
   - The web browser fires events when certain things happen on the page
   - We can detect events with JS using an event listener
   - The ` .addEventListener() ` method lets us listen for events on a DOM element
    ```javascript
    document.addEventListener("click", () => {
    console.log("clicked")
    });
    ```
 * **addEventListener() takes 2 parameters:**
   - The name of the event to listen to (e.g. "click")
   - A handler function that JS calls when that event is fired on this element
   - JS passes an event object to the handler function with information about the event
   - `event.target` is the element the event fired on
* **"click" isn't the only type of event we can handle**
  - "dblclick"
  - "mouseover"
  - "mouseout"



## Coding Examples

```javascript
let globalVariable = "I live in global scope"; 
function narrowerScope() {
    console.log(globalVariable);
    let localVariable = "I live in the function scope";
}
narrowerScope();
console.log(localVariable);
```
```javascript
output:
I live in global scope
Uncaught ReferenceError: localVariable is not defined
```



## Coding Exercises

### [Global Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions)

#### My Solution


```javascript
// Declare the myGlobal variable below this line
let myGlobal=10

function fun1() {
  // Assign 5 to oopsGlobal here
oopsGlobal=5;
}

// Only change code above this line

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}

```

### [Local Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions)

#### My Solution


```javascript
function myLocalScope() {
  // Only change code below this line
let myVar
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);

```

### [Global vs. Local Scope in Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions)
#### My Solution


```javascript
// Setup
const outerWear = "T-Shirt";

function myOutfit() {
  // Only change code below this line
const outerWear = "sweater";
  // Only change code above this line
  return outerWear;
}

myOutfit();
```

### [Stand in Line](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/stand-in-line)
#### My Solution


```javascript
function nextInLine(arr, item) {
  // Your code here

   let arr2 = arr.push(item);

   item = arr.shift();

  return item;  // Change this line
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));

```

