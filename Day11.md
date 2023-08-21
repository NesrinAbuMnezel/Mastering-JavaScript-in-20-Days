
# Day 11: 
## Types
* **Primitive Types**
  - undefined
  - string
  - number
  - boolean
  - symbol
  - null
  - bigint
* **Objects**
  - function
  - array
  - object
    
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/3fcabc2c-ffd3-49ee-8e9b-b1567878f82f"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/d7e2b2c9-15bb-4748-9a93-469d52efa981"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/0b6ed34b-8bf5-49c3-b5c5-e10fa2b32685"/><br/>
  
  
## Coercion
* **Abstract Operations**
  - ToPrimitive
  - ToString
    
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/bb71655f-8863-404d-9701-ed522145c370"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/f075cd3a-0366-4ea0-ba26-b57c794bf678"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/2b357fc4-16f0-4be4-827b-ebc1c7c6daba"/><br/>
 - ToNumber
   
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/7214fb74-c4de-4681-abc1-6028be4654d7"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/3b8ecff7-4136-4e06-829e-a37e0eb326cd"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/52839594-03ce-42e9-9499-8f8e8f60aa04"/><br/>
 - ToBoolean
   
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/deac4a15-08cd-4ba4-8508-9d154dd87f94"/><br/>



* **corner cases of Coercion**
<br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/fb2a1df1-d39f-4a1e-b8eb-6bed3887b09d"/><br/>
<img width="50%" height="40%" src="https://github.com/NesrinAbuMnezel/Mastering-JavaScript-in-20-Days/assets/95749191/a0adbad9-b572-4b9a-87ad-3e2778edde5c"/><br/>


## Coding Exercises
## Question 1:

Write a function called `convertStringToNumber` that converts a string to a
number using the unary plus operator. 

If the input is not a string, return an object of the input's value and type.

#### My Solution


```javascript
function convertStringToNumber(input) {
  //write your own code here
}
```


-------------------------------------------------------------------

## Question 2:

Write a function called `checkNaN` that takes a single argument and returns
`true` if the argument is `NaN` and `false` otherwise. 


#### My Solution


```javascript
const checkNaN = (value) => {
  //write your own code here
}
```
-------------------------------------------------------------------

## Question 3: 

Write a function called `isEmptyValue` that checks if a given input is an empty value (undefined,
null, or empty string). 


#### My Solution


```javascript
function isEmptyValue(value) {
  //write your own code here
}
```


-------------------------------------------------------------------

## Question 4: 

Write a function called `compareObjects` that takes 2 arguments of type
`"object"` and compares them. If both arguments are equal, return `true`. If
not, return `false`.

If either argument is not of type `"object"`, the function should return an
array of the arguments. 


#### My Solution


```javascript
function compareObjects(input1, input2) {
  //write your own code here
}
```

-------------------------------------------------------------------

## Question 5: 

Write a function called `complexCoercion` that takes a single argument and
checks if its type is primitive, and if so returns a coerced value according to
the rules below.

coercion rules: 
- if input is primive and:
  - if input is a number, convert to string and then return a boolean. 
  - if input is a string, return a boolean.
  - if input is `null` or `undefined`, return `false`.

If input is not a primitive type, return the argument.


#### My Solution


```javascript
const complexCoercion = (input) => {
  //write your own code here
}
```

