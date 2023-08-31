
# Day 14: 
## Advanced Scope
*  Lexical scope care where a function was declared, but dynamic scope cares where a function was called from
*  The Temporal Dead Zone is a behavior in JavaScript that occurs when trying to access a variable before it has been declared.

    
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/8cfd241c-ca74-4bac-b6e1-fab84f279fc7"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/2af09576-8964-487b-8f6a-8f529256869b"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/d64e1c74-0618-4aee-b5bc-9a7e589dd759"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/a7841e9a-d3c6-43aa-a489-41d1b7a9b8ea"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/74bec29a-8e40-4ab0-9a9a-2fb9be255730"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/657634cf-769b-4eb7-9271-f7a6c2ae32f4"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/a739bcb3-e9ae-4b1c-b5a0-94412ed6c97d"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/ce9df3c9-49a7-45e2-900b-6776b7b20b55"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/9429d752-3da9-4a1f-b7d9-08558b5a7e3c"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/f84ef4b2-96fe-4b9c-861d-83d4a2cf4246"/><br/>



## Coding Exercises
### QUESTION #1

Given the following code snippet and **explain what's happening**.

```javascript
for (var i = 0; i < 5; i++) {
    setTimeout(function() {
      console.log("value of [i] is: ", i);
    }, 100);
}
```

The current output is: "value of [i] is: 5" five times.

The output should be: 

"value of [i] is: ", 0 "value of [i] is: ", 1 "value of [i] is: ", 2 "value of
[i] is: ", 3 "value of [i] is: ", 4

Without changing anything in the for loop's code itself, provide a solution to
fix it.
#### My Solution
```javascript
for (var i = 0; i < 5; i++) {
    (function(i) {
        setTimeout(function() {
            console.log("value of [i] is: ", i);
        }, 100);
    })(i);
}

```
-------------------------------------------------------------------

### QUESTION #2

Given the following code snippet and **explain what's happening**. 

```javascript

for (let i = 0; i < 5; i++) {
   let array = [];
   array.push(i);
   console.log("Current array is: ", array)
}

```

The current output is: 

"Current array is: [ 0 ]" "Current array is: [ 1 ]" "Current array is: [ 2 ]"
"Current array is: [ 3 ]" "Current array is: [ 4 ]".

The output should be: "Current array is: [0, 1, 2, 3, 4]".

Provide a solution to fix it. 
#### My Solution
```javascript
let array = []; 

for (let i = 0; i < 5; i++) {
   array.push(i); 
}

console.log("Current array is: ", array); 

```
-------------------------------------------------------------------

### QUESTION #3

Given the following code snippet and **explain what's happening**. 

```javascript

let functions = [];

for (var i = 0; i < 5; i++) {
  functions.push(() => {
    console.log("Current value of i is:", i);
  });
}

functions.forEach((func) => func());

```

The current output is: 

"Current value of i is: 5" "Current value of i is: 5" "Current value of i is: 5"
"Current value of i is: 5" "Current value of i is: 5"

The output should be: 

"Current value of i is: 0" "Current value of i is: 1" "Current value of i is: 2"
"Current value of i is: 3" "Current value of i is: 4"

Provide a solution to fix it. 
#### My Solution
```javascript
let functions = [];

for (let i = 0; i < 5; i++) {
  functions.push(() => {
    console.log("Current value of i is:", i);
  });
}

functions.forEach((func) => func());

```
