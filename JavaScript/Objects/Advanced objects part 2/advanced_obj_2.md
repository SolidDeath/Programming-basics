# Advanced JavaScript Objects Part 2

## 1. Explanation

### Object Destructuring:

Destructuring assignment is a special syntax that allows us to “unpack” arrays or objects into a bunch of variables, as sometimes that's more convenient. Destructuring also works great with complex functions that have a lot of parameters.

```
let options = {
  title: "Menu",
  width: 100,
  height: 200
};

let {title = "default", width = 50, height = 50} = options;

console.log(title);  // Menu
console.log(width);  // 100
console.log(height);  // 200
```

### Spread Operator with Objects:

The Spread Operator allows us to spread out elements of an iterable (like an array or an object) across another array or object. When spreading objects, if the objects have a common property, the value from the last spread object is the one that's used.

```
let obj1 = { foo: 'bar', x: 42 };
let obj2 = { foo: 'baz', y: 13 };

let clonedObj = { ...obj1 }; // Object { foo: "bar", x: 42 }
let mergedObj = { ...obj1, ...obj2 }; // Object { foo: "baz", x: 42, y: 13 }
```

### Computed Property Names:

Now with computed property names in ES6, you can now directly use a variable as your property key in your object literal. Additionally, you can derive computed properties from expressions.

```
let propKey = 'foo';

let obj = {
  [propKey + 'bar']: 'Hey'
};

console.log(obj.foobar);  // Hey
```

### Object methods (`Object.assign()`, `Object.keys()`, `Object.values()`, `Object.entries()`, `hasOwnProperty()`):

JavaScript provides us with a collection of built-in methods to interact with objects. Note that `Object.assign()` only creates a shallow copy of the object, hence, nested objects are copied as references.

```
let obj = { foo: 'bar', x: 42, y: 50 };

console.log(Object.keys(obj));  // ['foo', 'x', 'y']
console.log(Object.values(obj));  // ['bar', 42, 50]
console.log(Object.entries(obj));  // [['foo', 'bar'], ['x', 42], ['y', 50]]
console.log(obj.hasOwnProperty('foo'));  // true

let obj2 = Object.assign({}, obj);  // creates a shallow copy of obj
console.log(obj2);  // { foo: 'bar', x: 42, y: 50 }
```

### Using `Object.create()` to implement prototypal inheritance:

`Object.create()` is used to create a new object and set the prototype of the new object to the original object. Properties can be added in the second argument of `Object.create()`.

```
let person = {
  isHuman: false,
  printIntroduction: function() {
    console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
  }
};

let me = Object.create(person, { 
  name: {value: 'Matthew'}, 
  isHuman: {value: true} 
});

me.printIntroduction();  // My name is Matthew. Am I human? true
```

## 4. Exercise Tasks

### Easy Level:

Use destructuring assignment to swap the values of two variables 'a' and 'b'. 'a' and 'b' are properties of the same object.

### Medium Level:

Use the spread operator to combine two objects into one. The objects should have at least one common property.

### Hard Level:

Use a computed property name to set the property of an object based on the value of a variable.

### Very Hard Level:

Create a 'Person' object with properties 'name' and 'age' and a method 'greeting'. Then, use `Object.create()` to create another object that inherits from 'Person', change its properties, and call the 'greeting' method.