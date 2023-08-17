
# Day 10: 
## Classes & Prototypes
* ****
  - 
  - 
 

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
    // Our code is getting repetitive, we're breaking our DRY principle. And suppose we have millions of users!
    What could we do?

   
   ```
  ![1](https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/1a514b4d-0ddc-4d8c-b0ad-2b780780dcff)


     



## Coding Exercises

### [Object Oriented Programming challenge](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/#object-oriented-programming)

#### My Solution
### [Object Oriented Programming challenge](https://www.freecodecamp.org/Nesrin)





