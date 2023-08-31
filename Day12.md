
# Day 12: 
## Equality
* **== vs. ===**
  - == checks value (loose)
  - === checks value and type (strict)

    
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/691cc723-8324-4134-86e1-8f77c9ed87ae"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/948a610a-9407-4467-9114-0acaac3f3ee4"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/15e6ee97-d57e-4ba6-b890-f52eacbf9fb0"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/db9fe365-0028-4da1-bf0d-4e33429529bb"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/5cd0020f-aad1-4a0a-8faa-2d14dd3a8a3b"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/a04f7249-f4ca-4940-822f-946075cc0407"/><br/>

## Static Typing
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/a87c0907-b3ac-4afb-8fd4-87904bad8141"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/b7a565c1-0c4b-4b16-80a9-74f54ee33b35"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/5021dc1b-7152-4763-951a-38317b1491d2"/><br/>



## Coding Exercises
### QUESTION #1

Given the following `promisesArray`, convert the array into an object using the
`convertToObj` function.

You should apply typescript types to every promise, the input of `convertToObj`,
and the output of `convertToObj`. 

Build interfaces and types as needed.

```javascript

const sayHelloWorld = new Promise(resolve, reject => {
  resolve("Hello world!");
});

const checkBoolean = (boolean) => new Promise(resolve, reject => {
  if (boolean) {
    resolve(boolean);
  } else {
    reject(`Input is false :(`)
  }
})

const returnObj = new Promise(resolve, reject => {
  resolve({
    x: "meow",
    y: 45,
  })
})

const promisesArray = [sayHeloWorld, checkBoolean, returnObj];

const convertToObj = (array) => {
  //write your code here;
  return obj;
}

```
#### My Solution
```javascript

```

-------------------------------------------------------------------

### QUESTION #2:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript
function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();

```
**Choices:**

A) `undefined`, `undefined`, `undefined`   
B) `1`, `undefined`, `ReferenceError`  
C) `1`, `ReferenceError`, `ReferenceError`   
D) `1`, `ReferenceError`

#### My Solution
```javascript

```
-------------------------------------------------------------------

### QUESTION #3:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript
function testScope2() {
  console.log(a);
  console.log(b);
  console.log(c);
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
}

testScope2();

```

**Choices:**

A) `undefined`, `ReferenceError`   
B) `1`, `undefined`, `ReferenceError`   
C)`undefined`, `undefined`,
`ReferenceError`  
D) `1`, `ReferenceError`

#### My Solution
```javascript

```
-------------------------------------------------------------------

### QUESTION #4:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript

function testScope3() {
  var a = 36;
  let b = 100;
  const c = 45;

  console.log([a, b, c]);

  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log([a, b, c]);
  }

  console.log([a, b, c]);
}

testScope3();

```

**choices:**

A) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 36, 2, 3 ]`   
B) `[ 36, 100, 45 ]` | `[1, 2, 3 ]` | `[ 36, 100, 45 ]`   
C) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1,100, 45 ]`   
D) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1, 2, 3 ]`
#### My Solution
```javascript

```
