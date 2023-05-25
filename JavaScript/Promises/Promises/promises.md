# JavaScript Promises

## 1. Explanation

In JavaScript, a Promise is an object representing the eventual completion or failure of an asynchronous operation. Essentially, it's a returned object to which you attach callbacks, instead of passing callbacks into a function.

A Promise is in one of these states:

- **pending**: initial state, neither fulfilled nor rejected.
- **fulfilled**: meaning that the operation completed successfully.
- **rejected**: meaning that the operation failed.

A pending promise can either be fulfilled with a value or rejected with a reason (error). Once a promise is fulfilled or rejected, it is immutable (i.e it can never change again).

Here's an example of a Promise:

```
let promise = new Promise(function(resolve, reject) {
  // the function is executed automatically when the promise is constructed

  // after 1 second signal that the job is done with the result "done"
  setTimeout(() => resolve("done"), 1000);
});

// react to the Promise resolution
promise.then(
  result => console.log(result), // shows "done!" after 1 second
  error => console.log(error) // doesn't run
);
```

## 2. Exercise Tasks

### First task:

1. Create a Promise that resolves with the message "Promise resolved" after 2 seconds.

### Second task:

2. Create a Promise that rejects with the message "Promise rejected" after 2 seconds.

### Third task:

3. Write a function that takes a number as input and returns a Promise that resolves with the square of the number after 2 seconds.

### Fourth task:

4. Write a function that takes a number as input and returns a Promise. If the input is greater than 10, the Promise should resolve with the result of the number divided by 2. If the input is less than or equal to 10, the Promise should reject with the message "Input must be greater than 10".