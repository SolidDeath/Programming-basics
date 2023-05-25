# JavaScript Async/Await

## 1. Explanation

Async/await is a new syntax for handling Promises in a more comfortable manner. Async/await is non-blocking, and it enables asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.

The `async` keyword is used to declare a function as asynchronous, and it operates on a promise. The `await` keyword is used in an `async` function to pause and wait for the Promise's resolution or rejection.

Here's an example of async/await:

```
async function foo() {
    let promise = new Promise((resolve, reject) => {
        setTimeout(() => resolve("Promise resolved!"), 1000)
    });

    let result = await promise; 

    console.log(result); // "Promise resolved!"
}

foo();
```

In this example, `foo()` is an async function that waits for the promise to resolve and then logs the result.

## 2. Exercise Tasks

### First task:

1. Create an async function that returns a resolved Promise with the message "Promise resolved".

### Second task:

2. Create an async function that returns a rejected Promise with the message "Promise rejected".

### Third task:

3. Write an async function that waits for the Promise from the third task of the previous lesson (Promise that resolves with the square of a number) and logs the result.

### Fourth task:

4. Write an async function that uses try/catch to handle errors for the Promise from the fourth task of the previous lesson (Promise that resolves if input > 10 and rejects otherwise).