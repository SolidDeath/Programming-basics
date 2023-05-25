# JavaScript DOM Manipulation

## 1. Explanation

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the structure of a document and enables a way to manipulate the structure, style, and content.

Here are some ways to manipulate the DOM:

### Selecting Elements

JavaScript can select HTML elements in several ways, including:

#### document.getElementById(id)

This method gets the element with the specific ID:

```
let elem = document.getElementById('my-id');
```

#### document.getElementsByClassName(name)

This method gets all elements with the specified class:

```
let elems = document.getElementsByClassName('my-class');
```

#### document.getElementsByTagName(name)

This method gets all elements with the specified tag:

```
let elems = document.getElementsByTagName('p');
```

#### document.querySelector(selector)

This method gets the first element that matches the CSS selector:

```
let elem = document.querySelector('#my-id');
```

#### document.querySelectorAll(selector)

This method gets all elements that match the CSS selector:

```
let elems = document.querySelectorAll('.my-class');
```

### Changing Content

#### innerHTML

The innerHTML property can get or set the HTML content within an element:

```
elem.innerHTML = 'New content';
```

#### textContent

The textContent property can get or set the text within an element:

```
elem.textContent = 'New text content';
```

### Changing Attributes

#### getAttribute(name)

The getAttribute method can get the value of an attribute:

```
let attr = elem.getAttribute('href');
```

#### setAttribute(name, value)

The setAttribute method can set the value of an attribute:

```
elem.setAttribute('href', 'https://www.example.com');
```

### Changing Styles

You can change the style of an element with the style property:

```
elem.style.color = 'blue';
```

### Adding and Removing Elements

#### createElement(tagName)

This method creates a new element:

```
let newElem = document.createElement('p');
```

#### appendChild(elem)

This method adds a new child element:

```
elem.appendChild(newElem);
```

#### removeChild(elem)

This method removes a child element:

```
elem.removeChild(childElem);
```

## 2. Exercise Tasks

### First task:

1. Write a JavaScript program that selects the HTML element with the ID of "demo" and changes its content.

### Second task:

2. Write a JavaScript program that creates a new paragraph and adds it to the end of the HTML document.

### Third task:

3. Write a JavaScript program that changes the color of all `<h1>` elements to blue.

### Fourth task:

4. Write a JavaScript program that removes every second paragraph in the HTML document.