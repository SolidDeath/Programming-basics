# Lesson: For Loops

In JavaScript, a "for loop" is a control flow statement that allows code to be repeatedly executed. A for loop is characterized by three statements (usually) enclosed in parentheses and separated by semicolons:

- The initialization statement: This is executed before the loop starts.
- The condition statement: The loop will continue as long as this condition is true.
- The final-expression statement: This is executed at the end of each loop iteration.

Here's the syntax:

```javascript
for ([initialization]; [condition]; [final-expression]) {
    // code block to be executed
}
```

The initialization statement is executed only once before the start of the loop. The condition statement is evaluated before each loop iteration. If it returns true, the loop continues; otherwise, the loop stops. After every iteration, the final-expression is executed.


## How to Use

You can access an element in the array like this: `arrayName[indexNumber]`

## Example and Output

Here's an example of creating an array, accessing an element, and changing an element:

```javascript
let fruits = ["Apple", "Banana", "Cherry"];

console.log(fruits[1]); // Outputs: Banana

fruits[1] = "Blueberry";
console.log(fruits); // Outputs: ["Apple", "Blueberry", "Cherry"]
```
## Exercise Tasks

### Easy level

    Create an array called "numbers" with five numbers and print it.

### Medium level

    Create an array called "colors" with five colors. Print the third color.

### Hard level

    Create an array called "animals" with three animals. Change the second animal to "cat" and print the array.

### Very hard level 

    Create an array "mixed" with different types of elements. The array should contain at least one string, one number, and one boolean.

