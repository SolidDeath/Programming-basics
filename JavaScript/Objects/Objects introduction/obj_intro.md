# JavaScript Objects

## 1. Explanation

In JavaScript, an object is a standalone entity, with properties and type. It is like a container that holds data which can be of any data type. Objects are created with curly braces {} and can be created using the `new Object()` statement, or simply by writing the object inside the curly braces.

```
let objectName = {
  key1: value1,
  key2: value2,
  key3: value3
};
```

## 2. How to Use

Properties of JavaScript objects can be accessed or set using the dot notation, or the bracket notation.

```
objectName.key1; // Accessing property using dot notation
objectName['key1']; // Accessing property using bracket notation
```

## 3. Example and Output

```
let car = {
  make: 'Tesla',
  model: 'Model 3',
  year: 2020
};

console.log(car.make);  // Output: Tesla
console.log(car['model']);  // Output: Model 3
```

## 4. Exercise Tasks

### Easy Level:

Create a JavaScript object named `book` with properties: `title`, `author`, and `year`.

### Medium Level:

Write a function that takes an object and a property key as parameters and returns the value of the property from the object.

### Hard Level:

Add a new property to the `book` object called `publisher` and set its value.
