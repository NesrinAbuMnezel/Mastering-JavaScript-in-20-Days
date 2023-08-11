
# Day 3: 
## Arrays
Arrays let us keep multiple values together in a single collection `let synonyms = ["plethora", "array", "cornucopia"];`
* **mutable vs. immutable**
  - "Mutable" data can be edited (e.g. Arrays)
  - "Immutable" data always stays the same (e.g. strings & other primitives)
  - Some actions "mutate" an array (e.g. oldArray.push(newValue))...aka change the array in-place
  - Other actions do not mutate the original array, but instead create a new copy (e.g. oldArray.concat(otherArray))
## Objects
Objects collect multiple values together to describe more complex data,objects let us point at related values using properties in the object.
* **Built in objects**
  - document
  - console
  - Math
## Quiz Project


## Coding Examples




## Coding Exercises

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

### [Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)

#### My Solution


```javascript
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence=['learning',...fragment,'is','fun']; // Change this line
  return sentence;
}

console.log(spreadOut());

```

### [Profile Lookup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)

#### My Solution


```javascript
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
   let msg;; 
  for (let i=0; i<contacts.length; i++) {
    if (contacts[i].firstName === name) {
      msg = contacts[i];
      break;
    }
  }
  if (msg) {
    if (msg.hasOwnProperty(prop)) {
      return msg[prop];
    } else {
      return "No such property";
    }
  } else {
    return "No such contact";
  }
  }
lookUpProfile("Akira", "likes");

```

### [Write Reusable JavaScript with Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/write-reusable-javascript-with-functions)

#### My Solution


```javascript
function reusableFunction(){
  console.log('Hi World')
}
reusableFunction()

```

### [Understanding Undefined Value returned from a Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understanding-undefined-value-returned-from-a-function)

#### My Solution


```javascript
// Setup
let sum = 0;

function addThree() {
  sum = sum + 3;
}
function addFive() {
  sum = sum + 5;
}

// Only change code below this line


// Only change code above this line

addThree();
addFive();

```

### [Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)

#### My Solution


```javascript
function timesFive(num){
return num*5
}
const answer=timesFive(5)

```
