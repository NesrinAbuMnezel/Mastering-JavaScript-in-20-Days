
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

### Functions and Callbacks

```javascript
Implement a JavaScript function called mapAsync that takes an array and a callback function. The function should map each element of the array to a new value using the callback function asynchronously.

The final result should be returned as a Promise.
```

#### My Solution


```javascript
true  // compare the value
false // compare the value and data type
true  // the first ! convert string to boolean the second one ! invert the false to true
```



### Call Stack and Recursion

```javascript
Write a JavaScript function called sumRange that calculates the sum of all integers in a given range. The function should use recursion to handle the calculation and demonstrate understanding of the call stack.
```



#### My Solution
```javascript
39 // here the priority for multiplication, so 5 * "7" , JS trying to convert to "7" to number (Implicit Conversion) ,which give 35
then 35 plus 4 
```

-------------------------------------------------------------------






