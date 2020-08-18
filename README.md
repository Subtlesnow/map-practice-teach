# Array.prototype.map
## Learning Objectives
- Perform basic data transformations using Array.prototype.map() in Javascript.
- Identify the parameters that `map` accepts.
- Compare and contrast `map` vs `forEach`.
## Introduction:
### What:
From MDN: [Array.prototype.map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
> Map calls a provided callback function once for each element in an array, in order, and constructs a new array from the results. A callback is invoked only for indexes of the array which have assigned values (including undefined).

Today we will introduce the array method `.map()` which is used to transform arrays. This transformation may be as simple as multiplying each number in an array of numbers by a certain factor, concatenating an array of strings to create new array of strings, or building collections of elements in React.
There are certainly ways to perform these tasks using `for` or `while` loops,
both those solutions have the disadvantage of being complex to read and reason
about (we have to do a lot of thinking to understand the code).
### Why:
So why `.map()`? Map returns a new array from the array the original array and the original array will remain unaltered.
Array methods make transforming data in arrays easier. These methods are also a lot more flexible and powerful than
using a loop, with the additional benefit that they are generally considered easier to read.
## Review 
### `for` loop:
```js
let numbers = [1, 2, 3, 4, 5]
for(let i = 0; i < numbers.length; i++) {
  // Note: we are only printing each element and not returning each element
  console.log(numbers[i])
}
// 1 2 3 4 5
```
### Now let's review the `forEach` method and callbacks:
```js
let numbers = [1, 2, 3, 4, 5]
numbers.forEach(number => {
  // Note: we are only printing each element and not returning each element
  console.log(number)
})
// 1 2 3 4 5
```
#### Callback function.
A callback function, is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
```js
// const higherOrderFunction = (callback) => return callback()
```
*What is our callback function for our previous example?*
### Let's now return a new array from our `for` loop and our `forEach()` method.
```js
let numbers = [1, 2, 3, 4, 5]
let doubleNumbers = [];
numbers.forEach(function(number) {
doubleNumbers.push(number * 2)
});
console.log(doubleNumbers);
// [ 2, 4, 6, 8, 10 ]
```
## Wake up, it's Map Time!
```js
let new_array = arr.map(function callback(currentValue, index, array){
  return statement;
})
```
Map takes 1 callback function:
- Callback: Function that is called upon every element of the array map is called on. Each time the `callback` executes, the returned value is added to the `new_array`.
    **The callback function takes 3 parameters:**
    - Current Value: The current value being processed in the array:
    - Index (optional): The index of the current element being processed in the array.
    - Array(optional): The array `map` was called upon.
### I do:
Let's rewrite our previous `forEach` example but now with `.map()`.
```js
let numbers = [1, 2, 3, 4, 5]
let doubleNumbers = numbers.map(number => number * 2)
console.log(doubleNumbers)
// [ 2, 4, 6, 8, 10 ]
```
### We do:
Now let's use `map` to append a special character `*` to the end of each element in the provide array.
```js
let words = ["this", "is", "an", "array", "of", "strings"]
// You code here...
// Returns ['this*', 'is*', 'a*', 'special*', 'array*', 'of*', 'strings*']
```
### You do:
For the following exercises, please use this same object:
```js
const data = [
  {name: 'Marty', age: 34, city: 'Brooklyn'},
  {name: 'Mick', age: 28, city: 'LES'},
  {name: 'Meagan', age: 27, city: 'Jersey City'},
  {name: 'Raul', age: 35, city: 'Harlem'}
]
```
Exercise 1:
```js
// [ 'Marty', 'Mick', 'Meagan', 'Raul' ]
```
Exercise 2:
 Given the following array, return a new array of objects and name is the key and city is the value. i.e. `[{Marty: 'Brooklyn'}]
```js
const data = [
  {name: 'Marty', age: 34, city: 'Brooklyn'},
  {name: 'Mick', age: 28, city: 'LES'},
  {name: 'Meagan', age: 27, city: 'Jersey City'},
  {name: 'Raul', age: 35, city: 'Harlem'}
]
// Write code here:
// returned array of objects:[
//  { Marty: 'Brooklyn' },
//  { Mick: 'LES' },
//  { Meagan: 'Jersey City' },
//  { Raul: 'Harlem' }
// ]
```
## Review
  - When would we use `.map` over `forEach`?
  - Do we modify the existing array?
  - What are the parameters that the callback excepts?
