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

## Document Ready
```javascript
document.addEventListener('DOMContentLoaded', function (event) {
    // Your code to run since DOM is loaded and ready
    
});
```

### Document Ready for Slow Loading Els
```javasript
var readyStateCheckInterval = setInterval(function() {
    if (document.readyState === "complete") {
        clearInterval(readyStateCheckInterval);
        init();
    }
}, 10);
```

## Regular Expressions
Regular expressions are a way to describe patterns in string data. They form a small, ... A number of common character groups have their own built-in shortcuts.

By formulating a regular expression with a special syntax, you can
* search text a string
* replace substrings in a string
* extract information from a string

## IIFE
An **IIFE** (*Immediately Invoked Function Expression*) is a JavaScript function that runs as soon as it is **defined**.
```javascript
;(function (window, document, undefined) {

	// self invoking

})( window, document);
```

### IIFE Public API
```javascript
//Self invoking and return an object, will be global to access anywhere within the window
var myIIFE = myIIFE || {};
myIIFE = (function (w,d){
	function doSomething(){
	//do something;
	}
	return {
	   //returning an object, key:value (function)
	   doSomething: doSomething
	}
})(window, docuement)

document.addEventListener('DOMContentLoaded', function (event) {
    // Your code to run since DOM is loaded and ready
    var readyStateCheckInterval = setInterval(function () {
        if (document.readyState === 'complete') {
            clearInterval(readyStateCheckInterval);
            myIIFE.doSomething();//calling the return function
        }
    }, 10);
});
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
template literals (template strings)
arrow functions =>
```

### Template Literals (Template Strings)
```javascript
let name = "Tu";
console.log(`My name is ${name}`);
// My name is Tu
// Need backticks, `` and placholders, ${expression}
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
Regular Function
elements.map(function(element) { 
  return element.length; 
}); // this statement returns the array: [8, 6, 7, 9]

Arrow Function
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

### Arrays
#### Loop Through Get Values and Index
```javascript
const arr = [1, 2, 3, 4, 5];
for (let (index, value) of arr.entries()){
  // arr.entries()
  console.log(index, value);
 };
```

### For...in Loop
```javascript
// Output the index
const numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
for (const index in numbers) {
  console.log(numbers[index]);
}
```

### For...of Loop
```javascript
// Output the values
const numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
for (const number of numbers) {
  console.log(number);
}
```

### Arrays Numerical Sorting
```javascript
numArray.sort((a, b) => a - b); // For ascending sort
numArray.sort((a, b) => b - a); // For descending sort
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
