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

Sure! Here's the continuation of the README with additional explanations and examples:

---

### 43. **What is an IIFE (Immediately Invoked Function Expression)?**
   - An IIFE is a function expression that is defined and immediately invoked after its creation. It is often used to create a new scope to avoid polluting the global namespace.

   ```javascript
   (function() {
     console.log("I am an IIFE!");
   })();
   ```

### 44. **What is event delegation in JavaScript?**
   - Event delegation is a technique where a single event listener is added to a parent element to handle events for multiple child elements. It takes advantage of event bubbling to manage events more efficiently.

   ```javascript
   document.querySelector('#parent').addEventListener('click', function(e) {
     if (e.target && e.target.matches('button.className')) {
       console.log('Button clicked');
     }
   });
   ```

### 45. **What are `setInterval` and `clearInterval`?**
   - `setInterval` is used to repeatedly call a function with a fixed time delay between each call.
   - `clearInterval` is used to stop a function that was scheduled with `setInterval`.

   ```javascript
   const intervalId = setInterval(() => {
     console.log('This will print every 2 seconds');
   }, 2000);

   clearInterval(intervalId);  // Stops the interval
   ```

### 46. **What is the difference between synchronous and asynchronous code in JavaScript?**
   - Synchronous code is executed line-by-line, blocking subsequent operations until the current one is completed. Asynchronous code allows other operations to run while waiting for an operation to complete.

   Example of synchronous code:
   ```javascript
   console.log('First');
   console.log('Second');
   console.log('Third');
   ```

   Example of asynchronous code using `setTimeout`:
   ```javascript
   console.log('First');
   setTimeout(() => {
     console.log('Second');
   }, 1000);
   console.log('Third');
   ```

### 47. **What is a singleton pattern?**
   - The singleton pattern ensures that a class has only one instance and provides a global point of access to that instance.

   ```javascript
   class Singleton {
     constructor() {
       if (!Singleton.instance) {
         Singleton.instance = this;
       }
       return Singleton.instance;
     }

     sayHello() {
       console.log('Hello!');
     }
   }

   const instance1 = new Singleton();
   const instance2 = new Singleton();
   console.log(instance1 === instance2);  // true
   ```

### 48. **What is memoization?**
   - Memoization is an optimization technique used to improve the performance of functions by caching previously computed results. If the function is called with the same arguments again, the cached result is returned.

   ```javascript
   function memoize(fn) {
     const cache = {};
     return function(x) {
       if (cache[x]) {
         return cache[x];
       }
       const result = fn(x);
       cache[x] = result;
       return result;
     };
   }

   const fib = memoize(function(n) {
     if (n <= 1) return n;
     return fib(n - 1) + fib(n - 2);
   });

   console.log(fib(10));  // Calculates Fibonacci value for 10 and caches intermediate results
   ```

### 49. **What are closures and how are they used?**
   - A closure is a function that retains access to variables from its lexical scope, even after the function that created those variables has finished execution. Closures are useful for data privacy and creating functions that remember their environment.

   ```javascript
   function outer() {
     let count = 0;
     return function inner() {
       count++;
       console.log(count);
     };
   }

   const increment = outer();
   increment();  // 1
   increment();  // 2
   ```

### 50. **What is the difference between `let` and `var` in JavaScript?**
   - `let` is block-scoped, meaning it is accessible only within the block it is declared. `var` is function-scoped, meaning it is accessible within the function it is declared.
   
   Example:
   ```javascript
   if (true) {
     let x = 10;
     var y = 20;
   }
   console.log(x);  // Error: x is not defined
   console.log(y);  // 20
   ```

### 51. **What is the purpose of the `bind` method?**
   - The `bind` method creates a new function that, when called, has its `this` value set to the provided value and prepends any provided arguments.

   ```javascript
   function greet(name) {
     console.log(`Hello, ${name}!`);
   }

   const greetUser = greet.bind(null, 'John');
   greetUser();  // Hello, John!
   ```

### 52. **What is destructuring in JavaScript?**
   - Destructuring is a syntax that allows you to unpack values from arrays or properties from objects into distinct variables.

   ```javascript
   // Array destructuring
   const [a, b] = [1, 2];
   console.log(a, b);  // 1 2

   // Object destructuring
   const {name, age} = {name: 'Alice', age: 25};
   console.log(name, age);  // Alice 25
   ```

### 53. **What is the spread operator (`...`) in JavaScript?**
   - The spread operator is used to expand elements from an iterable (like an array or object) into individual elements or properties.

   ```javascript
   // Array example
   const arr1 = [1, 2, 3];
   const arr2 = [...arr1, 4, 5];
   console.log(arr2);  // [1, 2, 3, 4, 5]

   // Object example
   const obj1 = {a: 1, b: 2};
   const obj2 = {...obj1, c: 3};
   console.log(obj2);  // {a: 1, b: 2, c: 3}
   ```

### 54. **What is a `WeakSet` in JavaScript?**
   - A `WeakSet` is similar to a `Set`, but it only holds *weak* references to the objects. This means that objects stored in a `WeakSet` can be garbage collected if there are no other references to them.

   ```javascript
   let obj = {};
   const weakSet = new WeakSet();
   weakSet.add(obj);
   obj = null;  // The object can be garbage collected
   ```

### 55. **What are arrow functions and their limitations?**
   - Arrow functions are a more concise way to write functions. They do not have their own `this`, but inherit it from the parent scope.

   ```javascript
   const add = (a, b) => a + b;
   console.log(add(2, 3));  // 5
   ```

   **Limitations of arrow functions:**
   - They cannot be used as constructors.
   - They do not have their own `this`, `arguments`, or `super`.

### 56. **What is an asynchronous iterator in JavaScript?**
   - An asynchronous iterator allows you to work with asynchronous data sources, such as streams, by providing `next()` method which returns a promise for each item.

   ```javascript
   async function* fetchData() {
     yield 'Data 1';
     yield 'Data 2';
     yield 'Data 3';
   }

   (async () => {
     for await (let data of fetchData()) {
       console.log(data);
     }
   })();
   ```

### 57. **What is the difference between `const` and `let`?**
   - `const` is used for variables whose values should not be reassigned, while `let` is used for variables that may be reassigned.

   ```javascript
   const a = 10;
   a = 20;  // Error: Assignment to constant variable

   let b = 10;
   b = 20;  // Works fine
   ```

Certainly! Here's the continuation of the questions and answers:

---

### 58. **What is a `Proxy` in JavaScript?**
   - A `Proxy` is an object that allows you to define custom behavior for fundamental operations (such as property lookup, assignment, and function invocation) on another object.

   ```javascript
   const target = {
     message: "Hello, world!"
   };

   const handler = {
     get: function(target, prop) {
       if (prop === "message") {
         return `${target[prop]} (Proxied)`;
       }
       return prop in target ? target[prop] : "Property not found";
     }
   };

   const proxy = new Proxy(target, handler);
   console.log(proxy.message);  // "Hello, world! (Proxied)"
   console.log(proxy.nonExistent);  // "Property not found"
   ```

### 59. **What is `Object.seal` in JavaScript?**
   - `Object.seal` prevents new properties from being added to an object and marks all existing properties as non-configurable. However, existing properties can still be modified (their values can change).

   ```javascript
   const obj = { name: 'Alice' };
   Object.seal(obj);

   obj.name = 'Bob';  // Works fine
   obj.age = 30;      // Fails silently (no new properties can be added)

   console.log(obj);  // { name: 'Bob' }
   ```

### 60. **What is `Object.freeze` in JavaScript?**
   - `Object.freeze` makes an object immutable. You can no longer add, delete, or modify properties of the object. The object's properties are also deeply frozen if they are objects themselves.

   ```javascript
   const obj = { name: 'Alice' };
   Object.freeze(obj);

   obj.name = 'Bob';  // Fails silently (cannot modify existing properties)
   obj.age = 30;      // Fails silently (cannot add new properties)

   console.log(obj);  // { name: 'Alice' }
   ```

### 61. **What are template literals in JavaScript?**
   - Template literals are a way to embed expressions inside strings, which can span multiple lines and interpolate variables.

   ```javascript
   const name = 'Alice';
   const greeting = `Hello, ${name}!`;
   console.log(greeting);  // "Hello, Alice!"

   const multiline = `This is
   a multi-line
   string.`;
   console.log(multiline);
   ```

### 62. **What are `set` and `map` in JavaScript?**
   - **Set**: A collection of unique values. It doesn't allow duplicates and the values are not indexed.
   - **Map**: A collection of key-value pairs where keys can be any data type, and it maintains the order of insertion.

   ```javascript
   // Set example
   const set = new Set([1, 2, 3, 3, 4]);
   console.log(set);  // Set { 1, 2, 3, 4 }

   // Map example
   const map = new Map();
   map.set('a', 1);
   map.set('b', 2);
   console.log(map.get('a'));  // 1
   ```

### 63. **What are `WeakSet` and `WeakMap` in JavaScript?**
   - **WeakSet**: Similar to `Set`, but it only holds *weak* references to its objects. These objects are garbage-collected when there are no other references to them.
   - **WeakMap**: Similar to `Map`, but its keys are weakly held, meaning they can be garbage collected when there are no other references to them.

   ```javascript
   const weakSet = new WeakSet();
   let obj = {};
   weakSet.add(obj);
   obj = null;  // The object can be garbage collected

   const weakMap = new WeakMap();
   weakMap.set(obj, 'value');
   ```

### 64. **What is the purpose of `async/await` in JavaScript?**
   - `async/await` is used to work with asynchronous code in a more synchronous-like fashion. `async` is used to define an asynchronous function, and `await` is used to pause the execution of code until a promise resolves.

   ```javascript
   async function fetchData() {
     let data = await fetch('https://api.example.com');
     let jsonData = await data.json();
     console.log(jsonData);
   }

   fetchData();
   ```

### 65. **What is a generator function in JavaScript?**
   - A generator function is a special kind of function that can be paused and resumed during execution. It uses the `function*` syntax and yields values one at a time.

   ```javascript
   function* generator() {
     yield 1;
     yield 2;
     yield 3;
   }

   const gen = generator();
   console.log(gen.next());  // { value: 1, done: false }
   console.log(gen.next());  // { value: 2, done: false }
   console.log(gen.next());  // { value: 3, done: false }
   console.log(gen.next());  // { value: undefined, done: true }
   ```

### 66. **What are higher-order functions in JavaScript?**
   - Higher-order functions are functions that can take other functions as arguments or return functions as results. This is a key concept in functional programming.

   ```javascript
   function greet(name) {
     return `Hello, ${name}`;
   }

   function processName(fn, name) {
     return fn(name);
   }

   console.log(processName(greet, 'Alice'));  // "Hello, Alice"
   ```

### 67. **What is `new` in JavaScript?**
   - The `new` keyword is used to create an instance of an object from a constructor function or class. It sets up the `this` value within the constructor and ensures the object is created.

   ```javascript
   function Person(name) {
     this.name = name;
   }

   const person = new Person('Alice');
   console.log(person.name);  // "Alice"
   ```

### 68. **What is `this` in JavaScript?**
   - `this` refers to the object that is currently executing the code. Its value is determined by how a function is called.

   ```javascript
   const person = {
     name: 'Alice',
     greet: function() {
       console.log(`Hello, ${this.name}`);
     }
   };

   person.greet();  // "Hello, Alice"
   ```

### 69. **What is the `bind` method used for?**
   - The `bind` method creates a new function that, when called, has its `this` value set to the specified value, and prepends any provided arguments to the original function.

   ```javascript
   const person = {
     name: 'Alice',
     greet: function(age) {
       console.log(`Hello, ${this.name}. You are ${age} years old.`);
     }
   };

   const greetAlice = person.greet.bind(person, 25);
   greetAlice();  // "Hello, Alice. You are 25 years old."
   ```

### 70. **What is the difference between `localStorage`, `sessionStorage`, and `cookies`?**
   - `localStorage` stores data without an expiration time and persists even after the browser is closed.
   - `sessionStorage` stores data for the duration of the page session and is cleared when the page is closed.
   - `cookies` store data that can be sent with HTTP requests and have an expiration time set by the server or the user.

   ```javascript
   // Example of localStorage
   localStorage.setItem('name', 'Alice');
   console.log(localStorage.getItem('name'));  // "Alice"
   ```

### 71. **What are the common array methods in JavaScript?**
   - **`map`**: Creates a new array by applying a function to each element.
   - **`filter`**: Creates a new array with all elements that pass the test.
   - **`reduce`**: Reduces the array to a single value based on a function.
   - **`forEach`**: Executes a function for each element.
   - **`find`**: Returns the first element that satisfies the condition.

   ```javascript
   const arr = [1, 2, 3, 4];

   const doubled = arr.map(x => x * 2);  // [2, 4, 6, 8]
   const even = arr.filter(x => x % 2 === 0);  // [2, 4]
   const sum = arr.reduce((total, num) => total + num, 0);  // 10
   ```

Certainly! Here are more questions and answers to extend your guide:

---

### 72. **What is the `Array.prototype.some` method?**
   - The `some` method tests whether at least one element in the array passes the provided test. It returns `true` if any element meets the condition, otherwise `false`.

   ```javascript
   const arr = [1, 2, 3, 4];
   const hasEven = arr.some(num => num % 2 === 0);
   console.log(hasEven);  // true (since 2 and 4 are even)
   ```

### 73. **What is the `Array.prototype.every` method?**
   - The `every` method tests whether all elements in the array pass the provided test. It returns `true` if all elements meet the condition, otherwise `false`.

   ```javascript
   const arr = [1, 2, 3, 4];
   const allEven = arr.every(num => num % 2 === 0);
   console.log(allEven);  // false (because 1 and 3 are not even)
   ```

### 74. **What is the difference between `slice` and `splice` in JavaScript?**
   - `slice` is used to extract a portion of an array without modifying the original array, while `splice` is used to modify the array by adding/removing elements.

   ```javascript
   // slice example
   const arr1 = [1, 2, 3, 4, 5];
   const sliced = arr1.slice(1, 4);
   console.log(sliced);  // [2, 3, 4]

   // splice example
   const arr2 = [1, 2, 3, 4, 5];
   arr2.splice(1, 2, 'a', 'b');
   console.log(arr2);  // [1, 'a', 'b', 4, 5] (removes 2 and 3, adds 'a' and 'b')
   ```

### 75. **What is the difference between `null` and `undefined` in JavaScript?**
   - `null` is an explicit assignment value representing "no value" or "empty object reference". `undefined` means a variable has been declared but has not been assigned a value.

   ```javascript
   let a;
   console.log(a);  // undefined

   let b = null;
   console.log(b);  // null
   ```

### 76. **What is the `reduce` method in JavaScript?**
   - The `reduce` method applies a function to each element in the array (from left to right) to reduce it to a single value.

   ```javascript
   const arr = [1, 2, 3, 4];
   const sum = arr.reduce((acc, num) => acc + num, 0);
   console.log(sum);  // 10
   ```

### 77. **What is event bubbling in JavaScript?**
   - Event bubbling is a process where an event propagates from the target element to the root of the document. Each parent element can capture the event as it bubbles up.

   ```javascript
   document.getElementById('child').addEventListener('click', function() {
     alert('Child clicked');
   });

   document.getElementById('parent').addEventListener('click', function() {
     alert('Parent clicked');
   });

   // Click on the child element will trigger both 'child' and 'parent' alerts.
   ```

### 78. **What is the difference between `===` and `==` in JavaScript?**
   - `===` is the strict equality operator that compares both value and type, while `==` is the loose equality operator that compares only values, performing type coercion if necessary.

   ```javascript
   console.log(2 === '2');  // false (different types)
   console.log(2 == '2');   // true (type coercion)
   ```

### 79. **What is a higher-order function in JavaScript?**
   - A higher-order function is a function that takes another function as an argument, returns a function, or both.

   ```javascript
   function processArray(arr, fn) {
     return arr.map(fn);
   }

   const arr = [1, 2, 3];
   const result = processArray(arr, x => x * 2);
   console.log(result);  // [2, 4, 6]
   ```

### 80. **What is `JSON.parse()` and `JSON.stringify()` in JavaScript?**
   - `JSON.parse()` converts a JSON string into a JavaScript object, while `JSON.stringify()` converts a JavaScript object into a JSON string.

   ```javascript
   const obj = { name: 'Alice', age: 25 };
   const jsonString = JSON.stringify(obj);
   console.log(jsonString);  // '{"name":"Alice","age":25}'

   const parsedObj = JSON.parse(jsonString);
   console.log(parsedObj);  // { name: 'Alice', age: 25 }
   ```

### 81. **What are the different ways to declare a function in JavaScript?**
   - There are several ways to declare a function in JavaScript, including:
     - Function declarations
     - Function expressions
     - Arrow functions

   ```javascript
   // Function declaration
   function greet() {
     console.log('Hello');
   }

   // Function expression
   const greetExpression = function() {
     console.log('Hello');
   };

   // Arrow function
   const greetArrow = () => {
     console.log('Hello');
   };
   ```

### 82. **What are `bind()`, `call()`, and `apply()` in JavaScript?**
   - These are methods that allow you to set the `this` context of a function.
     - `bind()`: Returns a new function with the specified `this` value.
     - `call()`: Immediately invokes the function with the specified `this` value and arguments.
     - `apply()`: Similar to `call()`, but takes arguments as an array.

   ```javascript
   function greet(name) {
     console.log(`Hello, ${name}`);
   }

   const greetBound = greet.bind(null, 'Alice');
   greetBound();  // "Hello, Alice"

   greet.call(null, 'Bob');  // "Hello, Bob"
   greet.apply(null, ['Charlie']);  // "Hello, Charlie"
   ```

### 83. **What is the purpose of `setTimeout()` in JavaScript?**
   - `setTimeout()` is used to execute a function after a specified delay.

   ```javascript
   setTimeout(() => {
     console.log('This will execute after 2 seconds');
   }, 2000);
   ```

### 84. **What is the purpose of `setInterval()` in JavaScript?**
   - `setInterval()` is used to execute a function repeatedly with a specified delay between each execution.

   ```javascript
   const intervalId = setInterval(() => {
     console.log('This will execute every 2 seconds');
   }, 2000);

   // To stop the interval
   clearInterval(intervalId);
   ```

### 85. **What is the event loop in JavaScript?**
   - The event loop is a mechanism that handles asynchronous operations in JavaScript. It constantly checks the call stack and the message queue, executing tasks from the queue when the stack is empty.

   ```javascript
   console.log('Start');
   setTimeout(() => {
     console.log('Timeout executed');
   }, 0);
   console.log('End');

   // Output:
   // Start
   // End
   // Timeout executed
   ```

### 86. **What are template literals in JavaScript?**
   - Template literals allow you to embed expressions inside string literals, using `${}`. They also allow multi-line strings.

   ```javascript
   const name = 'Alice';
   const greeting = `Hello, ${name}!`;
   console.log(greeting);  // "Hello, Alice!"

   const multiLine = `This is
   a multi-line
   string.`;
   console.log(multiLine);
   ```

### 87. **What is a promise chain in JavaScript?**
   - A promise chain is a sequence of `.then()` methods that are used to handle asynchronous operations in a sequential manner. Each `.then()` returns a new promise, allowing chaining.

   ```javascript
   Promise.resolve(1)
     .then(result => {
       console.log(result);  // 1
       return result + 1;
     })
     .then(result => {
       console.log(result);  // 2
       return result + 1;
     })
     .then(result => {
       console.log(result);  // 3
     });
   ```

### 88. **What is the difference between `forEach()` and `map()` in JavaScript?**
   - `forEach()` is used to execute a function on each element of an array, but it does not return a value.
   - `map()` is used to create a new array by applying a function on each element.

   ```javascript
   const arr = [1, 2, 3];

   arr.forEach(num => console.log(num));  // Logs each element

   const newArr = arr.map(num => num * 2);
   console.log(newArr);  // [2, 4, 6]
   ```

### 89. **What is the `new` keyword used for in JavaScript?**
   - The `new` keyword is used to create an instance of a constructor function or class.

   ```javascript
   function Person(name) {
     this.name = name;
   }

   const person1 = new Person('Alice');
   console.log(person1.name);  // "Alice"
   ```

Sure! Here are additional JavaScript-related questions and answers:

---

### 90. **What is a closure in JavaScript?**
   - A closure is a function that "remembers" its lexical scope, even when the function is executed outside of that scope. Closures allow a function to access variables from its outer function even after the outer function has finished executing.

   ```javascript
   function outer() {
     let count = 0;
     return function inner() {
       count++;
       console.log(count);
     };
   }

   const counter = outer();
   counter();  // 1
   counter();  // 2
   ```

### 91. **What is an IIFE (Immediately Invoked Function Expression)?**
   - An IIFE is a function expression that is defined and executed immediately. It is often used to create a private scope.

   ```javascript
   (function() {
     console.log('I am an IIFE');
   })();
   ```

### 92. **What are the `call()`, `apply()`, and `bind()` methods?**
   - These methods allow you to control the `this` value inside a function.
     - `call()` and `apply()` invoke the function immediately, but `apply()` passes arguments as an array, while `call()` passes arguments individually.
     - `bind()` returns a new function with a specified `this` context.

   ```javascript
   function greet(name, age) {
     console.log(`Hello ${name}, you are ${age} years old`);
   }

   greet.call(null, 'Alice', 25);  // Hello Alice, you are 25 years old
   greet.apply(null, ['Bob', 30]);  // Hello Bob, you are 30 years old

   const greetAlice = greet.bind(null, 'Alice');
   greetAlice(25);  // Hello Alice, you are 25 years old
   ```

### 93. **What are `Map` and `WeakMap` in JavaScript?**
   - `Map` is a collection of key-value pairs where both keys and values can be any data type. `WeakMap` is similar to `Map`, but the keys are weakly referenced, meaning they don't prevent garbage collection.

   ```javascript
   const map = new Map();
   map.set('key1', 'value1');
   console.log(map.get('key1'));  // 'value1'

   const weakMap = new WeakMap();
   const obj = {};
   weakMap.set(obj, 'value');
   console.log(weakMap.get(obj));  // 'value'
   ```

### 94. **What is the `Symbol` data type in JavaScript?**
   - `Symbol` is a primitive data type that is used to create unique identifiers for object properties. It is useful when you need to avoid name clashes in objects.

   ```javascript
   const symbol = Symbol('description');
   console.log(symbol);  // Symbol(description)
   ```

### 95. **What are `async` and `await` in JavaScript?**
   - `async` is used to declare a function that returns a `Promise`. `await` is used inside `async` functions to pause execution until the `Promise` resolves.

   ```javascript
   async function fetchData() {
     const response = await fetch('https://api.example.com');
     const data = await response.json();
     console.log(data);
   }
   ```

### 96. **What is the purpose of `Promise.all()` and `Promise.race()`?**
   - `Promise.all()` allows you to wait for multiple promises to resolve and returns a new promise with an array of results. `Promise.race()` resolves as soon as the first promise resolves (or rejects).

   ```javascript
   const promise1 = Promise.resolve('Hello');
   const promise2 = Promise.resolve('World');

   // Promise.all
   Promise.all([promise1, promise2]).then(results => {
     console.log(results);  // ['Hello', 'World']
   });

   // Promise.race
   Promise.race([promise1, promise2]).then(result => {
     console.log(result);  // 'Hello'
   });
   ```

### 97. **What is the `finally()` method in a Promise?**
   - The `finally()` method is used to execute a callback function when the promise is settled (resolved or rejected), regardless of the outcome.

   ```javascript
   const promise = new Promise((resolve, reject) => {
     resolve('Done!');
   });

   promise
     .then(result => console.log(result))  // 'Done!'
     .finally(() => console.log('Cleanup!'));  // 'Cleanup!'
   ```

### 98. **What is `Object.freeze()` in JavaScript?**
   - `Object.freeze()` is used to freeze an object, meaning its properties cannot be added, removed, or modified.

   ```javascript
   const obj = { name: 'Alice' };
   Object.freeze(obj);
   obj.name = 'Bob';  // This will not change the object
   console.log(obj.name);  // 'Alice'
   ```

### 99. **What are the differences between `let`, `const`, and `var` in JavaScript?**
   - `var` declares a variable globally or within a function scope (with function-level scoping), while `let` and `const` have block-level scoping. `const` is used to declare constants (variables whose values cannot be reassigned).

   ```javascript
   var a = 10;
   let b = 20;
   const c = 30;

   a = 15;  // Allowed
   b = 25;  // Allowed
   // c = 35;  // Error: Assignment to constant variable
   ```

### 100. **What is `this` in JavaScript?**
   - The `this` keyword refers to the object that is currently executing the code. Its value depends on how the function is called (e.g., globally, as an object method, etc.).

   ```javascript
   function showThis() {
     console.log(this);
   }

   const person = { name: 'Alice', showThis };
   person.showThis();  // Logs the 'person' object
   ```

### 101. **What is event delegation in JavaScript?**
   - Event delegation is a technique in which you attach a single event listener to a parent element instead of multiple listeners to individual child elements. This takes advantage of event bubbling.

   ```javascript
   document.getElementById('parent').addEventListener('click', function(event) {
     if (event.target && event.target.matches('button.classname')) {
       console.log('Button clicked!');
     }
   });
   ```

### 102. **What is the difference between `map()` and `forEach()` in JavaScript?**
   - `map()` creates a new array by applying a function to each element, while `forEach()` executes the function on each element but does not return a new array.

   ```javascript
   const arr = [1, 2, 3];

   const doubled = arr.map(x => x * 2);
   console.log(doubled);  // [2, 4, 6]

   arr.forEach(x => console.log(x * 2));  // Logs 2, 4, 6
   ```

### 103. **What is the purpose of `window.localStorage` and `window.sessionStorage`?**
   - `localStorage` is used to store data that persists across browser sessions, while `sessionStorage` stores data only for the duration of the page session.

   ```javascript
   localStorage.setItem('username', 'Alice');
   console.log(localStorage.getItem('username'));  // 'Alice'

   sessionStorage.setItem('sessionData', 'xyz');
   console.log(sessionStorage.getItem('sessionData'));  // 'xyz'
   ```


---


