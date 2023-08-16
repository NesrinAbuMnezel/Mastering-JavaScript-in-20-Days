
# Day 8: 
## Closures
* ****
  - Functions get a new memory every run/invocation
  - When our functions get called, we create a live store of data (local memory/variable environment/state) for that function’s execution context.
  - When the function finishes executing, its local memory is deleted (except the returned value)
  - But what if our functions could hold on to live data between executions?
  - This would let our function definitions have an associated cache/persistent memory
  - But it all starts with us returning a function from another function

    ```javascript
    
   
    
    ```
  

     

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


