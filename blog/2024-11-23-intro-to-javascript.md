---
slug: intro-to-javascript
title: Intro to JavaScript
authors: Saad 
tags: [javascript]
---

![JavaScript logo](img/intro-to-javascript.png)

# JavaScript Tutorial Part 1

JavaScript is a versatile and powerful programming language essential for web development. Whether you are building interactive websites, server-side applications, or even mobile apps, understanding JavaScript is a must.

<!-- truncate -->

## Why Learn JavaScript?

JavaScript powers the dynamic behavior on most websites you visit daily. By learning JavaScript, you can:
- Create interactive web pages.
- Build dynamic web applications.
- Understand the foundational language for frameworks like React, Angular, and Vue.

> *Brendan Eich (Creator of JavaScript):* JavaScript is the only programming language that I know of that has a mental health problem.

---

### JavaScript Basics

#### Setting Up
1. **Using a Browser Console**
    Open your browser’s Developer Tools (F12 or right-click > Inspect > Console tab) to write and test simple JavaScript code.

2. **Using an Editor**
    Install an editor like [Visual Studio Code](https://code.visualstudio.com/) and set up an `.html` file with a `<script>` tag.

## JavaScript Data Types

### Primitive Data Types

1. **String**
    ```javascript
    let name = "Othmane";
    console.log(name); // Output: Othmane
    ```

2. **Number**
    ```javascript
    let age = 25;
    console.log(age); // Output: 25
    ```

3. **Boolean**
    ```javascript
    let isStudent = true;
    console.log(isStudent); // Output: true
    ```

4. **Null**
    ```javascript
    let emptyValue = null;
    console.log(emptyValue); // Output: null
    ```

5. **Undefined**
    ```javascript
    let uninitializedValue;
    console.log(uninitializedValue); // Output: undefined
    ```

6. **Symbol**
    ```javascript
    let uniqueId = Symbol("id");
    console.log(uniqueId); // Output: Symbol(id)
    ```

7. **Object**
    ```javascript
    let person = { name: "Othmane", age: 25 };
    console.log(person.name); // Output: Othmane
    ```

8. **Array**
    ```javascript
    let fruits = ["apple", "banana", "cherry"];
    console.log(fruits[1]); // Output: banana
    ```

## JavaScript Examples: All-in-One Code

```javascript
// Function Declaration
function greet(name) {
     return `Hello, ${name}!`;
}
console.log(greet("Othmane")); // Output: Hello, Othmane!

// Arrow Function
const greetArrow = (name) => `Hello, ${name}!`;
console.log(greetArrow("Mouad")); // Output: Hello, Mouad!

// Array Access
let fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // Output: apple

// Add Elements to an Array
fruits.push("orange");
console.log(fruits); // Output: ["apple", "banana", "cherry", "orange"]

// Remove the Last Element
fruits.pop();
console.log(fruits); // Output: ["apple", "banana", "cherry"]

// Add Elements to the Beginning of an Array
fruits.unshift("mango");
console.log(fruits); // Output: ["mango", "apple", "banana", "cherry"]

// Remove the First Element
fruits.shift();
console.log(fruits); // Output: ["apple", "banana", "cherry"]

// Map Function: Transform Array Elements
let numbers = [1, 2, 3, 4];
let doubled = numbers.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8]

// Filter Function: Get Even Numbers
let evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```