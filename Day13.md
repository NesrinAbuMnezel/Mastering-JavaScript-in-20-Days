
# Day 13: 
## Scope
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/5b9cd1ba-5f79-4d26-ad5f-67e314c3f5a2"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/10aa016f-54c0-4d96-8af2-a8e53523b5f6"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/a93c11af-2d5d-4d22-83f9-48703d8d9846"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/7c86f35c-1e28-43bd-bb60-0be34c7fae2f"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/f1cce897-1a57-44a9-8281-efc7601468c9"/><br/>


## Scope & Function Expressions
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/b0f29fc6-1bde-4a29-b892-4a4f1747d8f1"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/8aec3b52-1543-49ca-ae6e-8e2d212b0651"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/21187418-27d2-4550-88d4-b50cdf0aba18"/><br/>


## Coding Exercises

### QUESTION #1

Create a function called `arrowHOF` that takes an arrow function as input and
returns a new arrow function that enhances the behavior of the input function. 

The enhanced function should accept additional arguments and execute the input
function multiple times based on these arguments.


```javascript

const exampleNormalFunc1 = (a, b, c) => {
  return a * (b + c);
}

const exampleNormalFunc2 = (x, y) => {
  return x * y;
}

const exampleNormalFunc3 = (string) => {
  return string + " " + string + " " + string + "!";
}


const arrowHOF = (normalFunc) => {
  // write your code here;
}

const hofNormalFunc1 = arrowHOF(exampleNormalFunc1);
const hofNormalFunc2 = arrowHOF(exampleNormalFunc2);
const hofNormalFunc3 = arrowHOF(exampleNormalFunc3);

console.log(hofNormalFunc1(3, 4, 5)(2)); // logs 60 twice
console.log(hofNormalFunc2(20, 35))(4); // logs 700 four times
console.log(hofNormalFunc3("Meow")()); // logs "Meow Meow Meow!" once

```
#### My Solution
```javascript

```

-------------------------------------------------------------------

### QUESTION #2

Build a function called `preserveThis` that takes a function as input and
returns a new arrow function that behaves the same way as the input function but
preserves the original this context when used as a method of an object.

```javascript

// Example object
const obj = {
  name: 'John',
  greet: function (greeting) {
    console.log(`${greeting}, ${this.name}!`);
  }
};

const preserveThis = (func) => {
  // write your code here;
  return func;
}

// Wrap the greet function using preserveThis
const preservedGreet = preserveThis(obj.greet);

// Call the wrapped function as a method of the object
preservedGreet('Hello'); // Output: "Hello, John!"

```
#### My Solution
```javascript

```

-------------------------------------------------------------------

### QUESTION #3

Consider the 2 following examples and distinguish the different output in each
one with them with a reasoning.

**Example 1:**

```javascript
function outer1() {
  var x = 10;

  var inner1 = function() {
    console.log(x);
  };

  inner1();
}

outer1(); // Output: 10
```

> **Reasoning for example 1's output:**  
> .................................................................................

--------
#### My Solution
```javascript

```

**Example 2:**

```javascript
function outer2() {
  var x = 10;

  var inner2 = function() {
    var x = 20;
    console.log(x);
  };

  inner2();
}

outer2(); // Output: 20
```

> **Reasoning for example 2's output:**  
> .................................................................................
#### My Solution
```javascript

```
