
# Day 10: 
## Classes & Prototypes
 ```javascript

    // Objects - store functions with their associated data!
    // This is the principle of encapsulation - and it’s going to transform how we can ‘reason about’ our code
    const user1 = {
     name: "Will",
     score: 3,
     increment: function() { user1.score++; }
    };
    user1.increment(); //user1.score -> 4
    // Let's keep creating our objects. What alternative techniques do we have for creating objects?
   
    
 ```
  ```javascript
    // Creating user2 user dot notation
    const user2 = {}; //create an empty object
    //assign properties to that object
    user2.name = "Tim";
    user2.score = 6;
    user2.increment = function() {
     user2.score++;
    };

   
  ```
   ```javascript
    // Creating user3 using Object.create
    // Object.create is going to give us fine-grained control over our object later on
    const user3 = Object.create(null);
    user3.name = "Eva";
    user3.score = 9;
    user3.increment = function() {
     user3.score++;
    };
    // Our code is getting repetitive, we're breaking our DRY principle. And suppose we have millions of users! What could we do?

   
   ```
  ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/1a514b4d-0ddc-4d8c-b0ad-2b780780dcff)

  ```javascript
    // Solution 1. Generate objects using a function
function userCreator(name, score) {
 const newUser = {};
 newUser.name = name;
 newUser.score = score;
 newUser.increment = function() {
 newUser.score++;
 };
 return newUser;
};
const user1 = userCreator("Will", 3);
const user2 = userCreator("Tim", 5);
user1.increment()
   
   ```
  ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/9563a9d5-52f1-4619-8832-2229e7ac7f1c)

* **Solution 1. Generate objects using a function**
  - Problems: Each time we create a new user we make space in our computer's memory for all our data and functions. But our functions are just copies
* **Solution 2: Using the prototype chain**
  - Store the increment function in just one object and have the interpreter, if it doesn't find the function on user1, look up to that object to check if it's there
  - Link user1 and functionStore so the interpreter, on not finding .increment, makes sure to check up in functionStore where it would find it
  - Make the link with Object.create() technique
 ```javascript
    // Solution 2: Using the prototype chain
  function userCreator (name, score) {
   const newUser = Object.create(userFunctionStore);
   newUser.name = name;
   newUser.score = score;
   return newUser;
  };
  const userFunctionStore = {
   increment: function(){this.score++;},
   login: function(){console.log("Logged in");}
  };
  const user1 = userCreator("Will", 3);
  const user2 = userCreator("Tim", 5);
  user1.increment();
   
   ```
  ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/6c94e3fa-7bec-4b64-8e60-2267fc2267f5)



  


## Coding Exercises

### [Object Oriented Programming challenge](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/#object-oriented-programming)

#### My Solution
### [Object Oriented Programming challenge](https://www.freecodecamp.org/Nesrin)





