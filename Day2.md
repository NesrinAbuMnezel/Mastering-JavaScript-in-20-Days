
# Day 2: 
## Values & Data Types
* **Values**
  - chunks of information we want to work with
  - that information (data) can be of different types
* **typeof**
  - it's an operator tells you the type of a value
* **JS has two kinds of data:**
  - Primitive types (e.g. strings, numbers)
  - Objects (e.g. document & friends)
* **Primitive data types**
  - string
  - number
  - boolean
  - undefined
  - null
* **Strings**
  - strings are  made of characters
* **indexOf**
  - returns the index of a specific character, and if the character does not exit it returns -1
  - returns At what index does this substring begin
* **includes**
  - returns if the string contain some other string
* **startsWith**
  - returns if the string  start with some other string
* **+**
  - Connecting strings together
* **toLowerCase**
  - returns the lowercase version of a string
## Operators
* **Arithmetic operators**
  - `+` add
  - `-` subtract
  - `*` multiply
  - `/` divide
* **Comparison operators**
  - `>` greater than
  - `<` less than
  - `>=` greater than or equal to
  - `<=` less than or equal to
* **Equality operators**
  - `===` equals (strict)
  - `==`  equals (loosey-goosey)
  - `!==` does not equal (strict)
  - `!=`  does not equal (loosey-goosey)
 ## Expressions
 an expression evaluates to a value
* **Variables**
  - Variables let us remember values
  - Declaring a variable `let bankruptcy;`
  - Assigning a variable
     ```
     let myDeclaredVariable;
      myDeclaredVariable = "so value, much wow";
     ```
  - Declaring & assigning at once `let myAssignedVariable = "such efficient, amaze";`
* **const**
  - declares & assigns a "constant" aka a variable that can't be changed `const myUnchangeableVariable = "Never gonna give you up";`
* **Statements vs. Expressions**
  - An expression "asks" JS for a value
  - A statement "tells" JS to do something (e.g. declare/assign a variable)
 

### Coding Examples
**Which data type is each of these values?**
  1. false
    `boolean`
  2. "true"
    `string`
  3. document.title
     `string`
  4. "some string".length
     `number`
  5. null
     `object`


## Coding Exercises

### QUESTION #1

Consider the following JavaScript code:

```javascript
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b);
console.log(b === c);
console.log(!!d);
```

What will be the output of each console.log statement? **_You MUST explain WHY_**.

#### My Solution
```
true  // compare the value
false // compare the value and data type
true  // the first ! convert string to boolean the second one ! invert the false to true
```

-------------------------------------------------------------------

### QUESTION #2:


Consider the following JavaScript expression:

```javascript
console.log(4 + 5 * "7");
```

What will be the output of this expression? **_You MUST explain the steps of evaluation taken by JS_**.

#### My Solution
```
39 // here the priority for multiplication, so 5 * "7" , JS trying to convert to "7" to number (Implicit Conversion) ,which give 35
then 35 plus 4 
```

-------------------------------------------------------------------

### QUESTION #3:

Evaluate the following expression:

```javascript
let result = 5 + 2 * 3 - 1;
```

What will be the output of this expression? **_You MUST explain the steps of evaluation taken by JS_**.

#### My Solution
```
10 // here the priority for multiplication, 5 + 6 - 1 we start from left to right
```

-------------------------------------------------------------------

### QUESTION #4:

Consider the following code:

```javascript
let x = 10;
let y = '10';
console.log(x == y);
console.log(x === y);
```
What will be the output of each `console.log` statement? **_You MUST explain WHY_**.

#### My Solution
```
true  // compare the value
false // compare the value and data type
```

-------------------------------------------------------------------

### QUESTION #5:

Given the code below:

```javascript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result);
```

What is the value of result? **_You MUST explain the steps of evaluation taken by JS_**

#### My Solution
```
true  // num > 10 (Implicit Conversion) so it gives true && true || false 
```
