
# Day 9: 
## Async JS 
* **Promises, Async & the Event Loop**
  - Promises - the most signficant ES6 feature
  - Asynchronicity - the feature that makes dynamic web applications possible
  - The event loop - JavaScript’s triage
  - Microtask queue, Callback queue and Web Browser features (APIs)
     ```javascript
      // A reminder of how JavaScript executes code
     const num = 3;
    function multiplyBy2 (inputNumber){
    const result = inputNumber*2;
    return result;
    }
    const output = multiplyBy2(num);
    const newOutput = multiplyBy2(10);
   
    ```
     ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/001b6800-ec74-43fd-b92a-de5acb48cc94)

     ![2](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/79437eb6-ea2d-4826-99a6-e1eee649a3e3)
    
* **JavaScript is:**
  - Single threaded (one command runs at a time)
  - Synchronously executed (each line is run in order the code appears)
     ```javascript
      // What if we try to delay a function directly using setTimeout?
      // setTimeout is a built in function - its first argument is the function to delay followed by ms to delay by
     function printHello(){
     console.log("Hello");
    }
    setTimeout(printHello,1000);
    console.log("Me first!");
   
    ```
     ![5](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/d4c5a5b4-5c60-4442-991f-f2d9c3fbb2e9)

     ![4](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/afa1a7b7-03ab-4ca6-bab0-e37053dfc0c7)

     
* **JavaScript is not enough - We need new pieces (some of which aren’t JavaScript at all)**
  - Our core JavaScript engine has 3 main parts:
     - Thread of execution
     - Memory/variable environment
     - Call stack
  - We need to add some new components:
     - Web Browser APIs/Node background APIs
     - Promises
     - Event loop, Callback/Task queue and micro task queue
       
     ![3](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/b9fb60dd-4a39-43a6-baf5-3f79a1c60e5f)

     ```javascript
      function printHello(){ console.log("Hello"); }
    function blockFor1Sec(){ //blocks in the JavaScript thread for
    1 sec }
    setTimeout(printHello,0);
    blockFor1Sec()
    console.log("Me first!");
   
    ```
     ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/5d342609-3179-4c74-8546-e998f57d17cd)
    
     ![2](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/15dc40b3-f9a1-41d1-a03d-4a078ba531a1)

## Promises
* **Using two-pronged ‘facade’ functions that both:**
  - Initiate background web browser work and
  - Return a placeholder object (promise) immediately in JavaScript
 

    ```javascript
    function display(data){
     console.log(data)
    }
    const futureData = fetch('https://twitter.com/will/tweets/1')
    futureData.then(display);
    
    console.log("Me first!");
   
    
    ```
      ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/c3c83a5c-5c2a-4884-9151-448878d143d6)

* **Promises**
  - Special objects built into JavaScript that get returned immediately when we make a call to a web browser API/feature (e.g. fetch) that’s set up to return promises(not all are)
  - Promises act as a placeholder for the data we expect to get back from the web browser feature’s background work
* **then method and functionality to call on completion**
  - Any code we want to run on the returned data must also be saved on the promise object
  - Added using .then method to the hidden property ‘onFulfilment’
  - Promise objects will automatically trigger the attached function to run (with its input being the returned data )
    
   ```javascript
   
    function display(data){console.log(data)}
    function printHello(){console.log("Hello");}
    function blockFor300ms(){/* blocks js thread for 300ms }
    setTimeout(printHello, 0);
    const futureData = fetch('https://twitter.com/will/tweets/1')
    futureData.then(display)
    blockFor300ms()
    console.log("Me first!");
   
    
    ```
     ![3](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/40a4dc24-176a-42fe-9ebb-9025f6839af7)
     ![2](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/ef045bd6-1c31-4930-bd99-36e5af4e0adb)

* **We have rules for the execution of our asynchronously delayed code**
  - Hold promise-deferred functions in a microtask queue and callback function in a task queue (Callback queue) when the Web Browser 
      Feature (API) finishes
  - Add the function to the Call stack (i.e. run the function) when Call stack is empty & all global code run (Have the Event Loop check this condition)
  - Prioritize functions in the microtask queue over the Callback queue


## Coding Exercises

### Question 1:

You are given a function `executeInSequenceWithCBs` and some code. The task is to
modify the `executeInSequenceWithCBs` function so that it runs and executes all
the tasks inside the asyncTasks array. 

The function should return an array of messages obtained from each task's
execution.

You are only allowed to change the `executeInSequenceWithCBs` function or add new
functions/code. You cannot modify the tasks' functions.

```javascript

const task1 = (cb) => setTimeout(() => {
  const message = "Task 1 has executed successfully!";
  cb(message);
}, 3000)

const task2 = (cb) => setTimeout(() => {
  const message = "Task 2 has executed successfully!";
  cb(message);
}, 0)

const task3 = (cb) => setTimeout(() => {
  const message = "Task 3 has executed successfully!";
  cb(message);
}, 1000)

const task4 = (cb) => setTimeout(() => {
  const message = "Task 4 has executed successfully!";
  cb(message);
}, 2000)

const task5 = (cb) => setTimeout(() => {
  const message = "Task 5 has executed successfully!";
  cb(message);
}, 4000)

const asyncTasks = [task1, task2, task3, task4, task5];

const executeInSequenceWithCBs = (tasks, callback) => {}

```
#### My Solution
```javascript
const task1 = (cb) => setTimeout(() => {
  const message = "Task 1 has executed successfully!";
  cb(message);
}, 3000)

const task2 = (cb) => setTimeout(() => {
  const message = "Task 2 has executed successfully!";
  cb(message);
}, 0)

const task3 = (cb) => setTimeout(() => {
  const message = "Task 3 has executed successfully!";
  cb(message);
}, 1000)

const task4 = (cb) => setTimeout(() => {
  const message = "Task 4 has executed successfully!";
  cb(message);
}, 2000)

const task5 = (cb) => setTimeout(() => {
  const message = "Task 5 has executed successfully!";
  cb(message);
}, 4000)

const asyncTasks = [task1, task2, task3, task4, task5];

 const executeInSequenceWithCBs = async (tasks, callback) => {
   let promise = tasks.map((task) => task(callback));
   let result = await Promise.all(promise);
   callback(result);
   return result;
 };

 executeInSequenceWithCBs(asyncTasks, msg => {
   console.log(msg);
 });

```


-------------------------------------------------------------------

### Question 2:

You are given a function called `executeInParallelWithPromises`, which takes an
array of APIs (represented by objects). 

Your task is to write code that fetches the data of each API in parallel using
promises. In Parallel means that the api which resolves first, returns its value
first, regardless of the execution order. 

The output of the `executeInParallelWithPromises` function should be an array
containing the results of each API's execution.

Each result should be an object with three keys: `apiName`, `apiUrl`, and
`apiData`..

```javascript
const apis = [
  {
    apiName: "products", 
    apiUrl: "https://dummyjson.com/products",
  }, 
  {
    apiName: "users", 
    apiUrl: "https://dummyjson.com/users",
  }, 
  {
    apiName: "posts", 
    apiUrl: "https://dummyjson.com/posts",
  }, 
  {
    apiName: "comments", 
    apiUrl: "https://dummyjson.com/comments",
  }
]

const executeInParallelWithPromises = (apis) => {}

```
#### My Solution
```javascript
 const apis = [
   {
       apiName: "products",
       apiUrl: "https://dummyjson.com/products",
   },
   {
       apiName: "users",
       apiUrl: "https://dummyjson.com/users",
   },
   {
       apiName: "posts",
       apiUrl: "https://dummyjson.com/posts",
   },
   {
       apiName: "comments",
       apiUrl: "https://dummyjson.com/comments",
   }
]


const executeInParallelWithPromises = (apis) => {
   let promise = apis.map(api => {
       return fetch(api.apiUrl)
           .then(response => { response.json() })
           .then(data => {
               return {
                   Name: api.apiName,
                   Url: api.apiUrl,
                   Data: data
               }
           })
   })

   return Promise.all(promise)
}

executeInParallelWithPromises(apis)
   .then(data=>console.log(data))
   .catch(err => console.log(err))

```
-------------------------------------------------------------------
### Question 3: 

You are given a function called `executeInSequenceWithPromises`, which takes an
array of APIs (represented by objects). 

Your task is to write code that fetches the data of each API sequentially (one
after the other) using promises. 

In Sequence means that the api which executes first, returns its value
first.

The output of the `executeInSequenceWithPromises` function should be an array
containing the results of each API's execution.

Each result should be an object with three keys: `apiName`, `apiUrl`, and
`apiData`.

```javascript

const apis = [
  {
    apiName: "products", 
    apiUrl: "https://dummyjson.com/products",
  }, 
  {
    apiName: "users", 
    apiUrl: "https://dummyjson.com/users",
  }, 
  {
    apiName: "posts", 
    apiUrl: "https://dummyjson.com/posts",
  }, 
  {
    apiName: "comments", 
    apiUrl: "https://dummyjson.com/comments",
  }
]

//modify and write your code here
const executeInSequenceWithPromises = (apis) => {}

```
#### My Solution
```javascript
const apis = [
   {
       apiName: "products",
       apiUrl: "https://dummyjson.com/products",
   },
   {
       apiName: "users",
       apiUrl: "https://dummyjson.com/users",
   },
   {
       apiName: "posts",
       apiUrl: "https://dummyjson.com/posts",
   },
   {
       apiName: "comments",
       apiUrl: "https://dummyjson.com/comments",
   }
]

const executeInSequenceWithPromises = async (apis) => {
   let result = []
   for (let api of apis){
       let response = await fetch(api.apiUrl)
       let data = await response.json()
       result.push({
           Name: api.apiName,
           Url: api.apiUrl,
           Data: data
       })
   }
   return result
}

executeInSequenceWithPromises(apis)
   .then(result=>console.log(result))
   .catch(err =>console.log(err))
```

