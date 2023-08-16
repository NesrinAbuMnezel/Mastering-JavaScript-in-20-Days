
# Day 8: 
## Closures
* **Closure**
  - Functions get a new memory every run/invocation
  - When our functions get called, we create a live store of data (local memory/variable environment/state) for that function’s execution context.
  - When the function finishes executing, its local memory is deleted (except the returned value)
  - But what if our functions could hold on to live data between executions?
    this would let our function definitions have an associated cache/persistent memory
    but it all starts with us returning a function from another function

    ```javascript

    function createFunction() {
     function multiplyBy2 (num){
     return num*2;
     }
     return multiplyBy2;
    }
    const generatedFunc = createFunction();
    const result = generatedFunc(3); // 6
   
    
    ```
      ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/6f718155-3c12-4c8c-9b5b-a7a085cb4f9f)


    ```javascript

    function outer (){
     let counter = 0;
     function incrementCounter (){
     counter ++;
     }
     incrementCounter();
    }
    outer();

    ```
       ![2](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/cfea4d1b-1235-4aef-a7a7-91d94ecd3d53)

       ![3](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/4ac97ee8-6049-42a4-be1b-a5d18cde1cdd)

     ```javascript

     function outer (){
     let counter = 0;
     function incrementCounter (){ counter ++; }
     return incrementCounter;
    }
    const myNewFunction = outer();
    myNewFunction();
    myNewFunction();


    ```
      ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/8b9f87f9-564f-4130-bf58-d60d3fd2279e)

      ![2](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/2c823f1e-0d98-4d25-90f8-c799f59c5f54)

* **The bond**
  -When a function is defined, it gets a bond to the surrounding Local Memory(“Variable Environment”) in which it has been defined
* **The ‘backpack’**
  - We return incrementCounter’s code (function definition) out of outer into global and give it a new name - myNewFunction
  - We maintain the bond to outer’s live local memory - it gets ‘returned out’ attached on the back of incrementCounter’s function definition.
  - So outer’s local memory is now stored attached to myNewFunction - even though outer’s execution context is long gone
  - When we run myNewFunction in global, it will first look in its own local memory first (as we’d expect), but then in myNewFunction’s ‘backpack’
* **What can we call this ‘backpack’?**
  - Closed over ‘Variable Environment’ (C.O.V.E.)
  - Persistent Lexical Scope Referenced Data (P.L.S.R.D.)
  - ‘Backpack’
  - ‘Closure’
  - The ‘backpack’ (or ‘closure’) of live data is attached incrementCounter (then to myNewFunction) through a hidden property known as [[scope]] which persists when the inner function is returned out
* **Closure gives our functions persistent memories and entirely new toolkit for writing professional code**
  - Helper functions: Everyday professional helper functions like ‘once’ and ‘memoize’
  - Iterators and generators: Which use lexical scoping and closure to achieve the most contemporary patterns for handling data in JavaScript
  - Module pattern: Preserve state for the life of an application without polluting the global namespace
  - Asynchronous JavaScript: Callbacks and Promises rely on closure to persist state in an asynchronous environment
     
## Async JS 



## Coding Exercises

### Question 1:


Write a closure named createCounter that takes an initial value start and returns a function. The returned function, when invoked, should increment the counter by 1 and return the updated value.


#### My Solution


```javascript
function createCounter(start){
    let counter =0 ;
    let increment=()=>counter++;
    
    return increment
}
let result=createCounter(1);
console.log(result)

```


-------------------------------------------------------------------

### Question 2:


Write a closure named calculateAverage that takes an array of numbers, nums, and returns a function. The returned function, when invoked, should calculate and return the average of the numbers in the array.


#### My Solution
```javascript
const  calculateAverage = (nums)=>{
    let average = ()=> nums.reduce((sum,num)=>sum+num,0)/nums.length
    return average
}
let result=calculateAverage([1,2,3]);
console.log(result)

```
-------------------------------------------------------------------

### Question 3:

Write a closure named powerOf that takes a base number base and returns a function. The returned function, when invoked with an exponent exp, should calculate and return the result of base raised to the power of exp.


#### My Solution


```javascript
const  powerOf = (base)=>{
    let exponent = (exp)=> base**exp
    return exponent
}

```


-------------------------------------------------------------------

### Question 4:

Write a closure named compose that takes multiple functions as arguments and returns a new function. The returned function should apply the provided functions in reverse order, passing the result of each function as an argument to the next function.

#### My Solution


```javascript

```


