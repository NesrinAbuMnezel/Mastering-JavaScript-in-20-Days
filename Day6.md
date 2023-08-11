
# Day 6: 
## Data Fetching & Promises
* **APIs**
  - Application Programming interfaces
  - APIs provide URLs that point at data we care about
  - fetch() lets us use JS to load data from APIs `fetch("https://dog.ceo/api/breed/hound/list")`
* **Promises**
  - Promises can be in 3 possible states:
     - `pending` : still waiting for the value, hang tight
     - `fulfilled` (aka "resolved"): finally got the value, all done
     - `rejected` : sorry couldn't get the value, all done
  - It takes time for Promises to resolve, so they are "asynchronous"
* **await**
  - tell JS to stop and wait for an asynchronous operation to finish
  - APIs provide URLs that point at data we care about
  - fetch() lets us use JS to load data from APIs `fetch("https://dog.ceo/api/breed/hound/list")`
  - The Promise we get from fetch() resolves to a Response object
  - .json() method on the response parses its body as a JSON object
## Destructing Data
* **Destructing**
  - Destructuring is a fancy way of declaring multiple variables at once
  - We can also destructure Arrays, assigning variables for their items `const [baby, ginger, scary, sporty, posh] = spices;`
  - We can use commas to "skip" values `const [,,melB] = spices;`
  - We can use ... to collect remaining values `const [babySpice, ...adultSpices] = spices;`
## Async
```javascript
async function fetchResponse(url) {
    const response = await fetch(url);
    return response;
}
```
This tells JS to expect to await async operations inside the function

## Modules
* **Module**
  - let us split big codebases across multiple files
    ```javascript
     <script type="module">
    //...
    </script>
    ```
  - One difference is that we can't use await outside of a function in a script
    ```javascript
    <script>
    await fetch("https://dog.ceo/api/breed/hound/list");
     </script>
    ```
  - Another difference is that modules create their own scope
* **import && export**
  - export lets us expose variables from our module's scope to the outside world
    ```javascript
     // myModule.js
     const veryUsefulFunction = () => "I came from a module";
     export { veryUsefulFunction };
    ```
  - import lets us use an exposed variable from another module
    ```javascript
     // otherModule.js
    import { veryUsefulFunction } from './myModule.js'
    veryUsefulFunction();
    ```
* **Debugging**
  - console.log() (or .warn() or .error()) is one way to understand what's happening when your program runs
    ```javascript
     function whyIsntThisWorking(input) {
    console.log("Well at least we got this far");
    console.log(input);
    return thingThatDoesntWork(input);
    }
    ```
  - You can also use the browser's debugger to pause JS and inspect what's happening
    ```javascript
     function whyIsntThisWorking(input) {
    debugger;
    return thingThatDoesntWork(input);
     } 
    ```
  - The debugger statement creates a breakpoint where JS will pause and let you look around
* **Error handling**
  - try lets us "watch out" for potential errors
  - catch lets us manage errors when they occur
    ```javascript
     try {
    thisMightThrowAnError();
     } catch (error) {
    console.error("As if! Error:", error); 
    console.log("Whatever, let's press on anyway");
    }
    console.log("still rollin' with the homies");
    ```
 



## Coding Exercises

### [Rick & Morty Characters List](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week1%20-%20javascript-from-first-steps-to-professional/day%206/task.md)

#### My Solution
### [Rick & Morty Characters List](https://github.com/NesrinAbuMnezel/Rick-Morty-)
![image](https://github.com/NesrinAbuMnezel/img/blob/main/Capture.PNG)

