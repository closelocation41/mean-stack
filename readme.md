# JavaScript Interview Questions

A collection of JavaScript interview questions and answers categorized by difficulty.

---

## Table of Contents
1. [Basic Questions](#basic-questions)
2. [Intermediate Questions](#intermediate-questions)
3. [Advanced Questions](#advanced-questions)
4. [Expert-Level Questions](#expert-level-questions)

---

## Basic Questions

1. **What are JavaScript data types?**
   - **Answer**: String, Number, Boolean, Undefined, Null, Object, Symbol, and BigInt.

2. **Explain `let`, `const`, and `var`.**
   - **Answer**:  
     - `var`: Function-scoped, can be redeclared.  
     - `let`: Block-scoped, cannot be redeclared.  
     - `const`: Block-scoped, used for constants, cannot be reassigned.

3. **What is the difference between `==` and `===`?**
   - **Answer**:  
     - `==`: Compares values after type coercion.  
     - `===`: Compares values without type coercion.

4. **What is the `typeof` operator?**
   - **Answer**: Returns the type of a variable or value (e.g., `"string"`, `"number"`).

5. **What is a closure in JavaScript?**
   - **Answer**: A closure is a function that retains access to its lexical scope even when executed outside that scope.

---

## Intermediate Questions

1. **What is the event loop?**
   - **Answer**: The event loop handles asynchronous code by queuing tasks in the call stack and message queue, allowing JavaScript to execute non-blocking operations.

2. **Explain `call`, `apply`, and `bind`.**
   - **Answer**:  
     - `call`: Invokes a function with a specific `this` and arguments passed individually.  
     - `apply`: Similar to `call`, but arguments are passed as an array.  
     - `bind`: Returns a new function with a specific `this` and optionally pre-filled arguments.

3. **What are promises in JavaScript?**
   - **Answer**: Promises represent the eventual result of an asynchronous operation, with three states: `pending`, `resolved`, and `rejected`.

4. **What is `hoisting` in JavaScript?**
   - **Answer**: Hoisting moves declarations (variables and functions) to the top of their scope before code execution.

5. **What is the difference between `null` and `undefined`?**
   - **Answer**:  
     - `null`: Explicitly set to represent "no value."  
     - `undefined`: Default value for uninitialized variables or missing object properties.

---

## Advanced Questions

1. **Explain prototypal inheritance in JavaScript.**
   - **Answer**: Objects in JavaScript inherit properties and methods from their prototype chain.

2. **What is the difference between synchronous and asynchronous programming in JavaScript?**
   - **Answer**:  
     - **Synchronous**: Code is executed sequentially, blocking the subsequent lines until the current one finishes.  
     - **Asynchronous**: Code allows non-blocking operations, enabling tasks to run concurrently (e.g., `setTimeout`, Promises, `async/await`).

3. **What is the difference between `function` declaration and `function` expression?**
   - **Answer**:  
     - **Function Declaration**: Defined with the `function` keyword and hoisted.  
     ```javascript
     function greet() {
         console.log("Hello");
     }
     ```  
     - **Function Expression**: Assigned to a variable and not hoisted.  
     ```javascript
     const greet = function () {
         console.log("Hello");
     };
     ```  

4. **What are JavaScript design patterns?**
   - **Answer**: Examples include:  
     - **Singleton**: Ensures a single instance of a class.  
     - **Observer**: Manages dependencies between objects (e.g., Event Listeners).  
     - **Factory**: Creates objects without exposing the instantiation logic.

5. **What is memoization?**
   - **Answer**: Memoization is a technique for optimizing function calls by caching previously computed results.

---

## Expert-Level Questions

1. **What is the difference between `Object.freeze` and `Object.seal`?**
   - **Answer**:  
     - **`Object.freeze`**: Prevents modifications to properties and values, making the object immutable.  
     - **`Object.seal`**: Prevents addition or deletion of properties but allows modification of existing properties.

2. **Explain the concept of shadow DOM.**
   - **Answer**: The shadow DOM is a part of Web Components that encapsulates styles and markup, ensuring they do not interfere with the main DOM.

3. **What is the `Reflect` API in JavaScript?**
   - **Answer**: The `Reflect` API provides methods to interact with object properties and prototypes, often used for meta-programming (e.g., `Reflect.get`, `Reflect.set`).

4. **What are generators in JavaScript?**
   - **Answer**: Generators are functions that can pause and resume execution using the `yield` keyword.  
   ```javascript
   function* generator() {
       yield 1;
       yield 2;
       yield 3;
   }
