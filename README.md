# Array.prototype.map Method

## Learning Objectives

- Perform basic data transformations using Array.prototype.map() in Javascript
- Compare and contrast when to use `map` vs `forEach`.

## The What and Why of using .map array method.

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

## Let's start off with a review of ways to iterate over each element in an array.

### First, we will review a `for` loop:

```js
let numbers = [1, 2, 3, 4, 5]
for(let i = 0; i < numbers.length; i++) {
  // Note: we are only printing each element and not returning each element
  console.log(numbers[i])
}
// 1 2 3 4 5
```

### Now let's review or `forEach` method:

```js
let numbers = [1, 2, 3, 4, 5]
numbers.forEach(number => {
  console.log(number)
})
// 1 2 3 4 5
```

### Let's now return a new array from our `for` loop and our `forEach()` method.

```js
let numbers = [1, 2, 3, 4, 5]
```

### Map

```js

```

### I do: --model thinking

### We do: --have students lead me in the exercise

### You do: --students show mastery by performing tasks

## Build in Check for Understanding

- List of questions
  - What is represented as our parameter for each element?
  - Do we modify the existing array?
  - What are more parameters that .map excepts?
  
  
