# Advanced JavaScript Functions

## 1. Explanation

JavaScript supports higher-level functions, which means functions can accept other functions as arguments, and functions can return functions. Advanced concepts in JavaScript functions include closures, IIFEs, higher-order functions, and arrow functions.

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
innerFunc();  // I'm outer var
```

### Immediately Invoked Function Expressions (IIFEs):

An IIFE is a function that runs as soon as it's defined.

```
(function() {
    console.log("This is an IIFE");
})();  // This is an IIFE
```

### Higher-order functions:

A higher-order function is a function that takes one or more functions as arguments, returns a function, or both.

```
// map is a higher-order function
let arr = [1, 2, 3, 4, 5];
let newArr = arr.map(function(num) { return num * 2 });
console.log(newArr);  // [2, 4, 6, 8, 10]
```

### Arrow functions:

Arrow functions provide a compact syntax to define functions in JavaScript. They also share the same lexical `this` as their surrounding code.

```
let arr = [1, 2, 3, 4, 5];
let newArr = arr.map(num => num * 2);
console.log(newArr);  // [2, 4, 6, 8, 10]
```

## 2. How to Use

### Closures:

Closures can be used when you want to give a function access to an outer function's scope.

```
function outer() {
    let outerVar = "I'm outer var";
    function inner() {
        console.log(outerVar);
    }
    return inner;
}

let innerFunc = outer();
innerFunc();  // I'm outer var
```

### IIFEs:

IIFEs can be used when you want to create a new scope, to avoid name collisions with other identifiers in the global scope.

```
(function() {
    let name = "John";
    console.log(name);  // John
})();

console.log(name);  // undefined
```

### Higher-order functions:

Higher-order functions can be used when you want to create more abstract functions, that can be customized with specific functions.

```
function greet(greeting) {
    return function(name) {
        console.log(greeting + ", " + name);
    };
}

let greetWithHello = greet("Hello");
greetWithHello("John");  // Hello, John
```

### Arrow functions:

Arrow functions can be used when you want to create a function with a compact syntax, or when you want to access the `this` value of the enclosing lexical context.

```
let arr = [1, 2, 3, 4, 5];
let newArr = arr.map(num => num * 2);
console.log(newArr);  // [2, 4, 6, 8, 10]
```

## 3. Exercise Tasks

### Easy Level:

Create an IIFE that logs "Hello, World!" to the console.

### Medium Level:

Write a higher-order function that takes a callback function and a string as arguments. The higher-order function should log the string to the console, then call the callback function.

### Hard Level:

Write a function that takes a string as an argument and returns a function. The returned function should take a number as an argument and repeat the string that number of times.

### Very Hard Level:

Write an arrow function that takes two parameters: an array of numbers and a number. The arrow function should return a new array that includes only numbers from the original array that are greater than the second parameter.

Please let me know the next topic you would like to cover.