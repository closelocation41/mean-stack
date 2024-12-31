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

Here is a detailed README file with answers and examples for the questions you mentioned:

---

## JavaScript & Node.js: Interview Questions and Answers

### 1. **Tell me about your background?**
   - I'm a software developer with over 6 years of experience specializing in backend and frontend technologies, cloud infrastructure, and business process automation. I have worked on impactful projects with companies like HCL and Cisco, and currently work with HCL as a lead engineer.

### 2. **What types of projects have you built?**
   - I have built web applications, business process automation systems, cloud-native applications, and e-commerce platforms, focusing primarily on Node.js, Angular, AWS, and MySQL.

### 3. **Is JavaScript single-threaded or multi-threaded?**
   - JavaScript is single-threaded, which means it processes one task at a time. However, asynchronous operations allow JavaScript to handle non-blocking tasks, such as I/O operations.

### 4. **How can we handle multiple asynchronous operations?**
   - We can handle multiple asynchronous operations using callbacks, promises, `async/await`, and `Promise.all`.

### 5. **What is a call stack?**
   - The call stack is a data structure that stores information about the function calls in a JavaScript program. It follows the Last In First Out (LIFO) principle, with the most recent function call being executed first.

### 6. **What is an event loop?**
   - The event loop is responsible for executing the code in JavaScript asynchronously. It continuously checks the message queue and moves tasks from the queue to the call stack when the stack is empty.

### 7. **What is a promise?**
   - A promise is an object that represents the eventual completion or failure of an asynchronous operation. It can be in one of three states: pending, resolved, or rejected.

### 8. **What is the difference between `Promise.all` and `Promise.allSettled`?**
   - `Promise.all` waits for all promises to be resolved and returns the results. If one promise is rejected, it immediately rejects.
   - `Promise.allSettled` waits for all promises to settle (either resolve or reject) and returns an array of results, including both resolved and rejected promises.

   ```javascript
   const promises = [Promise.resolve(1), Promise.reject(2)];

   Promise.allSettled(promises).then(results => console.log(results));
   ```

### 9. **What is an event emitter?**
   - An event emitter is an object that emits events and allows other objects to listen to these events. In Node.js, `EventEmitter` is used to handle events and callbacks.

### 10. **What are promises and observables?**
   - Promises represent the result of an asynchronous operation, while observables provide a stream of values over time. Observables are more powerful and flexible, especially when dealing with multiple asynchronous operations.

### 11. **What are caching optimization techniques?**
   - Caching can be optimized by using techniques such as caching only necessary data, caching frequently accessed data, using appropriate cache expiration, and leveraging distributed caching systems like Redis.

### 12. **What are general optimization techniques in JavaScript?**
   - Optimization techniques include minimizing DOM manipulation, using efficient algorithms, reducing memory usage, lazy loading assets, and bundling/minifying JavaScript code.

### 13. **What is the difference between `call` and `apply`?**
   - Both `call` and `apply` are used to invoke functions with a specific `this` context.
     - `call` accepts arguments individually.
     - `apply` accepts an array of arguments.

   ```javascript
   function greet(name) {
     console.log(`Hello, ${name}`);
   }

   greet.call(null, 'John'); // Hello, John
   greet.apply(null, ['John']); // Hello, John
   ```

### 14. **What is the difference between a `const` object and a frozen object (`Object.freeze`)?**
   - `const` makes the reference to the object constant, but the object itself can still be modified.
   - `Object.freeze` makes the object immutable, meaning its properties cannot be changed.

### 15. **What is the difference between `Map`, `Array`, and `WeakMap`?**
   - `Map` stores key-value pairs and allows any data type as a key.
   - `Array` is an ordered collection of elements.
   - `WeakMap` is similar to `Map` but allows keys to be garbage collected when they are no longer in use.

### 16. **What is the difference between `undefined` and `null`?**
   - `undefined` is a variable that has been declared but not assigned a value.
   - `null` is an intentional absence of any object value.

### 17. **What is the difference between `undefined` and an undeclared variable?**
   - `undefined` is a value assigned to a declared variable that hasn't been assigned a value.
   - An undeclared variable results in a ReferenceError when accessed.

### 18. **What do you know about hoisting in JavaScript?**
   - Hoisting is JavaScript's behavior of moving variable and function declarations to the top of their containing scope during compilation.

### 19. **What are JSON and AJAX libraries?**
   - JSON (JavaScript Object Notation) is a lightweight data interchange format.
   - AJAX (Asynchronous JavaScript and XML) allows data to be loaded asynchronously, and libraries like `axios` or `fetch` help manage AJAX requests.

### 20. **What code style do you typically follow?**
   - I follow standard JavaScript style guidelines, such as using `camelCase` for variables and functions, `PascalCase` for classes, and maintaining consistent indentation.

### 21. **What is your understanding of prototype functions and inheritance?**
   - JavaScript objects inherit properties and methods from their prototype. Prototypes allow objects to share methods, which is crucial for efficient memory usage.

### 22. **What is the difference between a constructor function and a prototype function?**
   - A constructor function is used to create objects and initialize their properties, while prototype functions are methods attached to the prototype of a constructor function.

### 23. **What is a reference? What is the difference between pass-by-value and pass-by-reference?**
   - A reference is an address in memory where a variable points to an object.
   - Pass-by-value means the function gets a copy of the value, whereas pass-by-reference means the function operates on the original data.

### 24. **What is a deep copy in JavaScript?**
   - A deep copy creates a new object and recursively copies all nested objects, unlike a shallow copy, which only copies the top-level properties.

### 25. **What is a deep-frozen object (`Object.freeze`)?**
   - A deep-frozen object is an object where all properties and nested objects are frozen using `Object.freeze` recursively.

### 26. **Why do we use the `this` operator in JavaScript?**
   - `this` refers to the current execution context, and it helps determine the context in which a function is executed.

### 27. **What is the difference between keyword functions and arrow functions?**
   - Arrow functions don’t have their own `this` context; they inherit `this` from the parent scope. Keyword functions have their own `this` context.

### 28. **What are `async/await` and generator functions?**
   - `async/await` provides a way to work with asynchronous code more synchronously.
   - Generator functions allow you to pause and resume function execution, useful for working with asynchronous operations.

### 29. **What is a `Symbol` in an object?**
   - A `Symbol` is a primitive data type used to create unique identifiers for object properties.

### 30. **How can we achieve multi-threading in Node.js?**
   - Multi-threading in Node.js can be achieved using Worker Threads or external modules like `cluster` for process-based concurrency.

### 31. **What is the V8 engine?**
   - The V8 engine is an open-source JavaScript engine developed by Google, used in Node.js and browsers like Chrome to execute JavaScript code.

### 32. **Why does Node.js use the V8 engine?**
   - Node.js uses the V8 engine because it provides fast execution of JavaScript code by compiling it into machine code.

### 33. **What is dependency injection?**
   - Dependency injection is a design pattern where dependencies (like services or components) are provided to a class instead of the class creating them itself.

### 34. **What is the difference between MySQL and MongoDB?**
   - MySQL is a relational database that uses SQL for querying, while MongoDB is a NoSQL database that stores data in JSON-like documents.

### 35. **Do you have experience with WebSockets?**
   - Yes, WebSockets provide full-duplex communication channels over a single TCP connection, ideal for real-time applications.

### 36. **How do you scale a Node.js application?**
   - Scaling Node.js applications can be achieved by clustering, load balancing, using microservices, and optimizing the event loop.

### 37. **How do you scale MongoDB?**
   - MongoDB can be scaled horizontally through sharding and vertically by increasing hardware resources.

### 38. **What are MongoDB and Redis?**
   - MongoDB is a NoSQL database, and Redis is an in-memory key-value store used for caching, session management, and pub/sub.

### 39. **What are `setTimeout` and `clearTimeout`?**
   - `setTimeout` schedules a function to be executed after a specified time delay. `clearTimeout` cancels a scheduled `setTimeout` function.

### 40. **Why should we use a separate Express app?**
   - A separate Express app allows for modularity, making it easier to manage routes, middleware, and configurations in large applications.

### 41. **What is the difference between `createStream` and `readFile` in Node.js?**
   - `createStream` returns a readable stream, allowing for more efficient reading of large files, while `readFile` reads a file entirely into memory.

### 42. **What is a closure in JavaScript?**
   - A closure is a function that retains access to its lexical scope, even when the function is executed outside of that scope.

---

This README provides detailed explanations with examples for each question. Feel free to modify it according to your specific needs.
