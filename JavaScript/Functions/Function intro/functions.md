# JavaScript functions
## Explanation:
Functions in JavaScript are one of the fundamental building blocks. A function is a JavaScript procedure—a set of statements that performs a task or calculates a value. A function is defined with the function keyword, followed by a name, followed by parentheses (()). The code to be executed by the function is placed inside curly brackets ({}).

## There are different ways to define a function:

### Function Declarations (Function Statements): 
A function declaration defines a named function. To create a function declaration, you use the function keyword followed by the name of the function.

```
function functionName() {
    // function body
}
```

### Function Expressions: 
A function expression is similar to and has the same syntax as a function declaration. One way in which they are commonly described as being different is that a function declaration gets hoisted and a function expression does not.

```
let functionName = function() {
    // function body
}
```
### Arrow Functions:
Arrow functions were introduced with ES6 as a new syntax for writing JavaScript functions. They save developers time and simplify function scope.

```
let sayWelcome = () => {
  console.log("Welcome, world!");
}
sayWelcome();
```
## How to Use:
You can use a function by calling it. For example, functionName(). If a function is taking parameters, you can pass those values while calling the function like functionName(param1, param2). Function returns the value using return keyword.

### Examples and Outputs:

Here are examples of function declarations, function expressions, and arrow functions:

#### Function Declarations (Function Statements):
```
function sayHello() {
    console.log("Hello, world!");
}
sayHello();
```
Output:

    Hello, world!

#### Function Expressions:
```
let sayGoodbye = function() {
    console.log("Goodbye, world!");
}
sayGoodbye();
```
Output:

    Goodbye, world!

#### Arrow Functions:

```
let sayWelcome = () => {
    console.log("Welcome, world!");
}
sayWelcome();
```
Output:

    Welcome, world!

## Exercise Tasks:
### Easy Level:
Write a function declaration called greet that takes a name as a parameter and logs a greeting message to that name.
### Medium Level:
Write a function expression called calculateArea that takes the length and width of a rectangle as parameters and returns the area of the rectangle.
### Hard Level:
Refactor your calculateArea function into an arrow function.
### Very Hard Level:
Write an arrow function called calculateFactorial that takes a number as a parameter and returns its factorial. The factorial of a number is the product of all positive integers less than or equal to that number. For example, the factorial of 5 is 5\*4\*3\*2\*1 = 120.

