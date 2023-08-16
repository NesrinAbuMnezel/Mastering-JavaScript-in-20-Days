
# Day 7: 
## JavaScript Principles
* **When JavaScript code runs, it:**
  - Goes through the code line-by-line and runs/ ’executes’each line - known as the **thread of execution**
  - Saves ‘data’ like strings and arrays so we can use that data later - in its **memory**
* **Execution context**
  - Created to run the code of a function
  - has 2 parts : Thread of execution , Memory
* **Call stack**
  - JavaScript keeps track of what function is currently running (where’s the thread of execution)
  - Run a function - add to call stack
  - Finish running the function - JS removes it from call stack
  - Whatever is top of the call stack - that’s the function we’re currently running 
    ```javascript
    
    const num = 3;
    function multiplyBy2 (inputNumber){
    const result = inputNumber*2;
    return result;
    }
    const output = multiplyBy2(num);
    const newOutput = multiplyBy2(10);
    
    ```
     ![Capture](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/5868ec25-9278-4e26-8654-993370b2e0e4)
    

    ![Capture1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/c73749a0-2776-4ced-9af6-450e0fa4d83a)


     

## Functions & Callbacks
* **Generalizing functions**
  - We may not want to decide exactly what some of our functionality is until we run our function
  - ‘Parameters’ (placeholders) mean we don’t need to decide what data to run our functionality on until we run the function
      then provide an actual value (‘argument’) when we run the function
   ```javascript
    
     function copyArrayAndMultiplyBy2(array) {
     const output = [];
     for (let i = 0; i < array.length; i++) {
     output.push(array[i] * 2);
     }
     return output;
     }
    const myArray = [1,2,3];
    const result = copyArrayAndMultiplyBy2(myArray);
    
    ```
   ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/56d43be8-ef95-4307-837c-6a7cb37d9b42)

   ![2](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/94281c20-25fc-4bd8-8481-4eb637db7254)
  
    What if want to copy array and divide by 2? Or add 3?
    We could generalize our function - So we pass in our specific instruction only when we run copyArrayAndManipulate !
  ```javascript
    
     function copyArrayAndManipulate(array, instructions) {
     const output = [];
     for (let i = 0; i < array.length; i++) {
     output.push(instructions(array[i]));
     }
     return output;
    }
    function multiplyBy2(input) { return input * 2; }
    const result = copyArrayAndManipulate([1, 2, 3], multiplyBy2);
    
    ```
     ![4](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/edb436a8-a61b-4d8a-acec-e99aeba12079)


    ![3](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/99e8c839-e1ac-4a9b-b7fb-484262f08a95)


   
* **first class objects**
  - Functions in javascript = first class objects
  - They can co-exist with and can be treated like any other javascript object
      - Assigned to variables and properties of other objects
      - Passed as arguments into functions
      - Returned as values from functions
* **Higher Order Function?**
  - The outer function that takes in a function is our higher-order function
  - Takes in a function or passes out a function
* **Callback Function**
  - The function we insert is our callback function
* **Callbacks and Higher Order Functions simplify our code and keep it DRY**
  - Declarative readable code: Map, filter, reduce - the most readable way to write code to work with data
  - Asynchronous JavaScript: Callbacks are a core aspect of async JavaScript, and are under-the-hood of promises, async/await
* **Anonymous and arrow functions**
  - Improve immediate legibility of the code
  - Understanding how they’re working under-the-hood is vital to avoid confusion


## Coding Exercises

### [Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)

#### My Solution


```javascript
const squareList = arr => {
  // Only change code below this line
  arr=arr.filter(s=>s>0 && Number.isInteger(s))
  arr=arr.map(s=>s*s)
  return arr;
  // Only change code above this line
};

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);

```
-------------------------------------------------------------------

### [Apply Functional Programming to Convert Strings to URL Slugs](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs)

#### My Solution


```javascript
// Only change code below this line
function urlSlug(title) {
let newTitle= title.trim().toLowerCase()
newTitle=newTitle.split(' ')
newTitle=newTitle.filter(s=>s!="").join("-")
title=`${newTitle}`
return title
}
// Only change code above this line
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");

```
-------------------------------------------------------------------

### Functions and Callbacks


Implement a JavaScript function called mapAsync that takes an array and a callback function.
The function should map each element of the array to a new value using the callback function asynchronously.
The final result should be returned as a Promise.


#### My Solution


```javascript

```


-------------------------------------------------------------------

### Call Stack and Recursion

Write a JavaScript function called sumRange that calculates the sum of all integers in a given range. 
The function should use recursion to handle the calculation and demonstrate understanding of the call stack.




#### My Solution
```javascript

```








