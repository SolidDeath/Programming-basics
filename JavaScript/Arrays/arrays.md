# JavaScript Arrays and Operations with Arrays

## 1. Explanation

An array in JavaScript is a high-level, list-like object used to be traversed and mutated. It can hold any type of values such as numbers, strings, objects, and even other arrays, and all values can be of mixed types.

Arrays are created with square brackets ([]), with elements separated by commas.

```
let arrayName = [element1, element2, element3];
```

## 2. How to Use

JavaScript provides many built-in methods to work with arrays. Here are some commonly used methods:

- ~`push()`~: Adds one or more elements to the end of an array and returns the new length of the array.
- ~`pop()`~: Removes the last element from an array and returns that element.
- ~`shift()`~: Removes the first element from an array and returns that element.
- ~`unshift()`~: Adds one or more elements to the front of an array and returns the new length of the array.
- ~`slice()`~: Returns a shallow copy of a portion of an array.
- ~`splice()`~: Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

## 3. Example and Output

```
let fruits = ['Apple', 'Banana', 'Mango'];

// Push
fruits.push('Orange');
console.log(fruits);

// Pop
fruits.pop();
console.log(fruits);

// Shift
fruits.shift();
console.log(fruits);

// Unshift
fruits.unshift('Strawberry');
console.log(fruits);

// Slice
let slicedFruits = fruits.slice(1, 3);
console.log(slicedFruits);

// Splice
fruits.splice(1, 0, 'Pineapple', 'Grapes');
console.log(fruits);
```

**Output:**

```
[ 'Apple', 'Banana', 'Mango', 'Orange' ]
[ 'Apple', 'Banana', 'Mango' ]
[ 'Banana', 'Mango' ]
[ 'Strawberry', 'Banana', 'Mango' ]
[ 'Banana', 'Mango' ]
[ 'Strawberry', 'Pineapple', 'Grapes', 'Banana', 'Mango' ]
```

## 4. Exercise Tasks

### Easy Level:

Create an array ~`numbers`~ and add the numbers from 1 to 5 using the ```push()``` method.

### Medium Level:

Remove the first number from the ```numbers``` array using the ```shift()``` method and log the result.

### Hard Level:

Use the ```slice()``` method to get the second and third numbers from the ```numbers``` array and log the result.

### Very Hard Level:

Write a function called ```rearrange``` that takes an array of numbers as a parameter and sorts the numbers in ascending order. Do not use the built-in ```sort()``` method for this task. Instead, use a sorting algorithm like bubble sort, selection sort, etc.