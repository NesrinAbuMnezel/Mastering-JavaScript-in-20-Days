
# Day 10: 
## JavaScript Principles
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
## Functions & Callbacks
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

## Coding Examples
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
```javascript
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
```javascript
39 // here the priority for multiplication, so 5 * "7" , JS trying to convert to "7" to number (Implicit Conversion) ,which give 35
then 35 plus 4 
```

-------------------------------------------------------------------



### [Copy Array Items Using slice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)

#### My Solution


```javascript
function forecast(arr) {
  // Only change code below this line
   arr=arr.slice(2,4);
  return arr;
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));

```


