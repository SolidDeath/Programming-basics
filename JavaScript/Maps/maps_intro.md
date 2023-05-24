# JavaScript Map

## 1. Explanation

In JavaScript, the Map object is a simple key-value map and can iterate its elements in insertion order. Unlike Objects, Maps accept keys of any type: functions, objects, primitive types, etc.

The Map object provides several useful methods and properties:

### Map Methods

- `map.set(key, value)` sets the value for the key in the map object. Returns the map object.

- `map.get(key)` returns the value for the key in the map object. If the key does not exist, it returns `undefined`.

- `map.has(key)` returns `true` if the key exists in the map, and `false` otherwise.

- `map.delete(key)` removes the element specified by the key. Returns `true` if the element is found and removed, and `false` otherwise.

- `map.clear()` removes all elements from the map.

- `map.size` returns the number of elements in the map.

Here are examples of these methods in action:

```
let map = new Map();
map.set('name', 'Alice');
map.set('age', 25);
map.set('job', 'Engineer');

console.log(map.get('name')); // Output: Alice
console.log(map.has('age')); // Output: true
console.log(map.size); // Output: 3

map.delete('job');
console.log(map.size); // Output: 2

map.clear();
console.log(map.size); // Output: 0
```

### Iterating Maps

The Map object can be iterated using various techniques:

- Map.entries(): Returns a new Iterator object that contains an array of [key, value] for each element in the Map object in insertion order.

- Map.keys(): Returns a new Iterator object that contains the keys for each element in the Map object in insertion order.

- Map.values(): Returns a new Iterator object that contains the values for each element in the Map object in insertion order.

Example of Map iteration:

```
let map = new Map();
map.set('name', 'Alice');
map.set('age', 25);
map.set('job', 'Engineer');

for(let [key, value] of map.entries()) {
    console.log(`${key}: ${value}`);
}
// Output: 
// name: Alice
// age: 25
// job: Engineer
```

## 2. Exercise Tasks

### First task:

1. Create a new Map, add some key-value pairs and retrieve a value.

### Second task:

2. Write a function that takes an array of [key, value] pairs and returns a new Map object.

### Third task:

3. Write a function that takes a Map and a key as arguments and checks whether the key exists in the Map.

### Fourth task:

4. Write a function that takes an array of numbers and returns a new array that contains each number from the original array only once. Do this by using a Map.