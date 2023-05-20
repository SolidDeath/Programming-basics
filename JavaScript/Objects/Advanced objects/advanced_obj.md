# Advanced JavaScript Objects

## 1. Explanation

JavaScript objects are not only able to store simple data types, but they can also hold functions. These functions are known as 'methods'. Methods are useful for actions that require object data. Inside the method definition, `this` refers to the object.

```
let objectName = {
  key1: value1,
  key2: function() {
    // some code here
  }
};
```

## 2. How to Use

### this Keyword:

In JavaScript, `this` is a special keyword that is used in methods to refer to the object that the method is acting upon.

```
let car = {
  make: 'Tesla',
  model: 'Model 3',
  displayCar: function() {
    return this.make + ' ' + this.model;
  }
};

console.log(car.displayCar());  // Output: Tesla Model 3
```

### Getters and Setters:

JavaScript also supports getter and setter methods in objects. The `get` syntax binds an object property to a function that will be called when that property is looked up, and `set` binds an object property to a function to be called when there is an attempt to set that property.

```
let book = {
  title: 'The Great Gatsby',
  author: 'F. Scott Fitzgerald',
  year: 1925,
  get summary() {
    return `${this.title} was written by ${this.author} in ${this.year}`;
  },
  set newYear(year) {
    this.year = year;
  }
};

console.log(book.summary);  // Output: The Great Gatsby was written by F. Scott Fitzgerald in 1925
book.newYear = 1926;
console.log(book.year);  // Output: 1926
```

### Object Prototypes:

In JavaScript, almost everything is an object, and all objects inherit properties and methods from a prototype. The `prototype` property allows you to add new methods or properties to object constructors.

```
function Book(title, author, year) {
  this.title = title;
  this.author = author;
  this.year = year;
}

Book.prototype.summary = function() {
  return `${this.title} was written by ${this.author} in ${this.year}`;
};

let book1 = new Book('The Great Gatsby', 'F. Scott Fitzgerald', 1925);
console.log(book1.summary());  // Output: The Great Gatsby was written by F. Scott Fitzgerald in 1925
```

## 4. Exercise Tasks

### Easy Level:

Create a JavaScript object 'student' with properties: 'name', 'class', and a method 'greeting' that returns 'Hello, my name is {name} and I'm in class {class}'.

### Medium Level:

Using the `this` keyword, create a method inside the 'student' object that changes the 'class' property.

### Hard Level:

Add a getter and a setter method to the 'student' object for the 'name' property.

### Very Hard Level:

Create a constructor function for a 'Student' object with properties 'name' and 'class'. Add a method to the 'Student' prototype that returns 'Hello, my name is {name} and I'm in class {class}'.