# Advanced JavaScript Functions

## 1. Explanation

JavaScript supports higher-level functions, which means functions can accept other functions as arguments, and functions can return functions. Advanced concepts in JavaScript functions include closures, IIFEs, higher-order functions, arrow functions and recursion.

### Closures:

In JavaScript, functions have access to their own scope (variables defined between their curly brackets), they also have access to the outer (enclosing) function's variables and parameters, and to the global variables. A closure is a function having access to the parent scope, even after the parent function has closed.

```
function outer() {
    let outerVar = "I'm outer var";
    function inner() {
        console.log(outerVar);
    }
    return inner;
}

let innerFunc = outer();
innerFunc();  // Output: I'm outer var
```

### Immediately Invoked Function Expressions (IIFEs):

An IIFE is a function that runs as soon as it's defined.

```
(function() {
    console.log("This is an IIFE");
})();  // Output: This is an IIFE
```

### Higher-order functions:

A higher-order function is a function that takes one or more functions as arguments, returns a function, or both.

```
// map is a higher-order function
let arr = [1, 2, 3, 4, 5];
let newArr = arr.map(function(num) { return num * 2 });
console.log(newArr);  // Output: [2, 4, 6, 8, 10]
```

### Arrow functions:

Arrow functions provide a compact syntax to define functions in JavaScript. They also share the same lexical `this` as their surrounding code.

```
let arr = [1, 2, 3, 4, 5];
let newArr = arr.map(num => num * 2);
console.log(newArr);  // Output: [2, 4, 6, 8, 10]
```

### Recursive functions:

In JavaScript, a function can call itself. This is known as a recursive function. Recursive functions can be used to solve problems where a task can be simplified into a simpler task of the same type.

```
function fibonacci(n) {
    if (n <= 1) {
        return n;
    } else {
        return fibonacci(n - 1) + fibonacci(n - 2);
    }
}
console.log(fibonacci(10));  // Output: 55
```

## 2. Exercise Tasks

### Easy Level:

Create an IIFE that logs "Hello, World!" to the console.

### Medium Level:

Write a higher-order function that takes a callback function and a string as arguments. The higher-order function should log the string to the console, then call the callback function.

### Hard Level:

Write a recursive function that calculates the factorial of a number. The factorial of a number is the product of all positive integers less than or equal to that number.

### Very Hard Level:

Write an arrow function that takes two parameters: an array of numbers and a number. The arrow function should return a new array that includes only numbers from the original array that are greater than the second parameter.
