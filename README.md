# JS
Javascript basics

Markdown basics
*This text will be italic*
**This text will be bold**
- [x] this is a **complete** item
- [ ] this is an incomplete item
- [x] @mentions, #refs, [links](http://github.com)

### Functions
```javascript
function rotate(matrix){
  return matrix;
};
```

### Function Expression
```javascript
var rotate = function(matrix){
  return matrix;
};
``` 

## Arrays
### Map
Creates a new array with the results of calling a provided function on **every** element in the calling array.
```javascript
var array1 = [1, 4, 9, 16];
// pass a function to map
const map1 = array1.map(x => x * 2);
// expected output of map1, a new array
[2, 8, 18, 32]
```

## ES6 Basics
```javascript
const for constants
let for block scope variables
arrow functions =>
```
### Arrow Functions
Two factors influenced the introduction of arrow functions: shorter functions and no existence of this keyword.
```javascript
var elements = [
  'Hydrogen',
  'Helium',
  'Lithium',
  'Beryllium'
];
Function
elements.map(function(element) { 
  return element.length; 
}); // this statement returns the array: [8, 6, 7, 9]

// The regular function above can be written as the arrow function below
elements.map((element) => {
  return element.length;
}); // [8, 6, 7, 9]

// When there is only one parameter, we can remove the surrounding parenthesies:
elements.map(element => {
  return element.length;
}); // [8, 6, 7, 9]

// When the only statement in an arrow function is `return`, we can remove `return` and remove
//  the surrounding curly brackets
elements.map(element => element.length); // [8, 6, 7, 9]
```

### ES6 Spread Operator?
```javascript
Spread Operator ...
Combine arrays, arr1.push(...arr2) // Adds arr2 items to end or array
Copy Arrays, like var arr2 = arr.slice(), var arr2 = [...arr]
```
```javascript
Math Functions
let numbers = [9, 4, 7, 1];
Math.min(...numbers); // 1
```
