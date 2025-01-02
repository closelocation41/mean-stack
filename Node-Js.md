## Technology Docs

- [Angular](Angular.md)  
- [MongoDB](MongoDB.md)  
- [MySQL](Mysql.md)  
- [Node.js](Node-Js.md)  
- [TypeScript](TypeScript.md)  
- [JavaScript](JavaScript.md)

Here is a list of 100+ interview questions with answers and examples for Node.js. These questions cover various topics like basics, advanced concepts, best practices, and frameworks.

### **Basic Node.js Interview Questions**
1. **What is Node.js?**
   - **Answer:** Node.js is an open-source, cross-platform JavaScript runtime environment built on Chrome's V8 JavaScript engine. It allows you to run JavaScript code on the server side.
   - **Example:** Running `console.log('Hello, World!')` on the server.

2. **What are the key features of Node.js?**
   - **Answer:** Asynchronous I/O, non-blocking, event-driven, single-threaded, scalable, built-in libraries, and cross-platform.

3. **What is the difference between Node.js and JavaScript?**
   - **Answer:** JavaScript is a programming language, while Node.js is a runtime environment that allows JavaScript to be run on the server-side.

4. **What is the Event Loop in Node.js?**
   - **Answer:** The Event Loop is a mechanism in Node.js that handles asynchronous callbacks. It allows Node.js to perform non-blocking operations despite being single-threaded.

5. **What is the role of `require()` in Node.js?**
   - **Answer:** `require()` is used to load external modules, such as libraries, built-in modules, or custom modules.

6. **Explain the concept of a Callback in Node.js.**
   - **Answer:** A callback is a function passed as an argument to another function, which is executed once the operation completes. Callbacks are commonly used for asynchronous operations.

7. **What is npm?**
   - **Answer:** npm (Node Package Manager) is a package manager for Node.js. It helps in installing, managing, and sharing libraries and packages in your Node.js applications.

8. **What is the difference between `process.nextTick()` and `setImmediate()` in Node.js?**
   - **Answer:** 
     - `process.nextTick()` defers the execution of a function until the next event loop cycle, before any I/O tasks.
     - `setImmediate()` schedules a function to execute after the current event loop cycle.

9. **What are Streams in Node.js?**
   - **Answer:** Streams are objects that allow reading or writing data in a continuous flow. There are four types of streams in Node.js: Readable, Writable, Duplex, and Transform.

10. **What is the difference between synchronous and asynchronous code in Node.js?**
    - **Answer:** Synchronous code blocks execution until the current operation completes, while asynchronous code does not block the event loop, allowing other operations to continue while waiting for a task to finish.

---

### **Intermediate Node.js Interview Questions**
11. **What is Express.js in Node.js?**
    - **Answer:** Express.js is a minimal and flexible web application framework for Node.js, used to build web servers and APIs with routing, middleware support, and various utility functions.

12. **What are middleware functions in Express.js?**
    - **Answer:** Middleware functions are functions that have access to the request, response, and next middleware function in the request-response cycle. They are used for various purposes like authentication, logging, error handling, etc.

13. **Explain the purpose of the `app.listen()` method in Express.**
    - **Answer:** `app.listen()` binds and listens for connections on a specified port. It creates a server to listen for incoming HTTP requests.

14. **What are Promises in Node.js?**
    - **Answer:** Promises are objects that represent the eventual result of an asynchronous operation. They allow chaining of `.then()` and `.catch()` for handling success or failure.

15. **What is a `callback hell`, and how can you avoid it?**
    - **Answer:** Callback hell occurs when multiple nested callbacks make code difficult to read and maintain. This can be avoided by using Promises or `async`/`await`.

16. **What is the `async/await` syntax in Node.js?**
    - **Answer:** `async/await` is a modern syntax for handling asynchronous operations. An `async` function always returns a promise, and `await` is used to wait for the resolution of a promise.

17. **Explain the role of `module.exports` and `exports` in Node.js.**
    - **Answer:** Both `module.exports` and `exports` are used to export objects, functions, or variables from a module. However, `module.exports` is the actual object that gets returned when the module is required, while `exports` is just a reference to `module.exports`.

18. **What is the `cluster` module in Node.js?**
    - **Answer:** The `cluster` module allows you to create child processes (workers) that can share server ports. It enables multi-core systems to take full advantage of the available CPU power.

19. **What is the `path` module in Node.js?**
    - **Answer:** The `path` module provides utilities for working with file and directory paths, such as joining, resolving, and normalizing paths.

20. **What is the difference between `fs.readFile()` and `fs.createReadStream()`?**
    - **Answer:** 
      - `fs.readFile()` reads the entire file into memory, which is suitable for small files.
      - `fs.createReadStream()` is used for reading large files in chunks, useful for streams.

---

### **Advanced Node.js Interview Questions**
21. **What are worker threads in Node.js?**
    - **Answer:** Worker threads allow you to execute JavaScript code in parallel threads, enabling true multi-threading in Node.js. This is useful for CPU-intensive tasks.

22. **How can you handle error handling in Node.js?**
    - **Answer:** Error handling can be done using try-catch blocks, handling rejected promises with `.catch()`, or using event emitters for error events.

23. **What is the purpose of `setTimeout()` and `setInterval()` in Node.js?**
    - **Answer:** 
      - `setTimeout()` is used to execute a function once after a specified delay.
      - `setInterval()` is used to execute a function repeatedly at specified intervals.

24. **What is an EventEmitter in Node.js?**
    - **Answer:** An EventEmitter is a class that allows you to create objects that can emit events and handle listeners for those events.

25. **What is the difference between `fs.readFile()` and `fs.open()` in Node.js?**
    - **Answer:** 
      - `fs.readFile()` reads the entire file into memory and then returns it.
      - `fs.open()` opens the file and returns a file descriptor, which can be used for reading or writing in a low-level way.

26. **How can you manage configuration settings in Node.js applications?**
    - **Answer:** You can use environment variables or configuration libraries like `dotenv` to manage settings.

27. **Explain the use of the `buffer` module in Node.js.**
    - **Answer:** The `buffer` module provides a way of handling raw binary data directly in memory. It is often used when dealing with I/O operations like reading files or network operations.

28. **What are the advantages of using Node.js for building web applications?**
    - **Answer:** Non-blocking asynchronous I/O, fast performance, scalability, and the ability to use JavaScript for both client and server-side development.

29. **How can you scale a Node.js application?**
    - **Answer:** You can scale a Node.js application using techniques like load balancing, clustering, microservices architecture, and horizontal scaling across multiple servers.

30. **What is the purpose of the `dotenv` module in Node.js?**
    - **Answer:** The `dotenv` module loads environment variables from a `.env` file into `process.env`, making it easier to manage configuration settings.

---

### **Additional Node.js Interview Questions**
31. **What is the use of the `http` module in Node.js?**
    - **Answer:** The `http` module is used to create HTTP servers and clients, handle HTTP requests, and send responses.

32. **What is the `url` module in Node.js?**
    - **Answer:** The `url` module provides utilities for parsing and formatting URLs.

33. **What is the `os` module in Node.js?**
    - **Answer:** The `os` module provides operating system-related utility methods, such as memory usage, CPU information, and platform details.

34. **What is the role of `require.cache` in Node.js?**
    - **Answer:** `require.cache` is an object that stores cached modules in Node.js to avoid reloading them multiple times.

35. **What are some commonly used debugging techniques in Node.js?**
    - **Answer:** Using `console.log()`, debugging with the `--inspect` flag in Chrome DevTools, or using the built-in Node.js debugger.
Here are additional Node.js interview questions, including explanations with coding examples:

---

### **Advanced Node.js Interview Questions with Code Examples**

36. **How does Node.js handle asynchronous code?**
    - **Answer:** Node.js uses an event-driven, non-blocking I/O model, which allows it to handle multiple operations simultaneously without waiting for any of them to finish.
    - **Example:**
      ```js
      const fs = require('fs');

      console.log('Start Reading File...');
      fs.readFile('example.txt', 'utf8', (err, data) => {
        if (err) throw err;
        console.log(data);  // Non-blocking, this will execute once the file is read.
      });
      console.log('File read request sent.');
      ```

---

37. **What is EventEmitter in Node.js and how does it work?**
    - **Answer:** The `EventEmitter` class in Node.js allows objects to emit events and listen for those events. It forms the core of how Node.js handles asynchronous events.
    - **Example:**
      ```js
      const EventEmitter = require('events');
      const myEmitter = new EventEmitter();

      // Listen for 'event' on myEmitter
      myEmitter.on('event', () => {
        console.log('Event triggered!');
      });

      // Emit the event
      myEmitter.emit('event');  // Output: Event triggered!
      ```

---

38. **What is a Promise in Node.js?**
    - **Answer:** A Promise represents the eventual completion (or failure) of an asynchronous operation and its resulting value. Promises are used to handle asynchronous operations more cleanly compared to callbacks.
    - **Example:**
      ```js
      const fetchData = new Promise((resolve, reject) => {
        const data = true;
        if (data) {
          resolve('Data fetched successfully!');
        } else {
          reject('Failed to fetch data.');
        }
      });

      fetchData
        .then(response => console.log(response))  // Output: Data fetched successfully!
        .catch(error => console.log(error));
      ```

---

39. **How do you create and manage child processes in Node.js?**
    - **Answer:** The `child_process` module allows you to spawn child processes in Node.js. This is useful for offloading heavy operations or running scripts in separate processes.
    - **Example:**
      ```js
      const { spawn } = require('child_process');
      const ls = spawn('ls', ['-lh', '/usr']);  // Spawning the `ls` command

      ls.stdout.on('data', (data) => {
        console.log(`stdout: ${data}`);
      });

      ls.stderr.on('data', (data) => {
        console.error(`stderr: ${data}`);
      });

      ls.on('close', (code) => {
        console.log(`child process exited with code ${code}`);
      });
      ```

---

40. **What are Streams in Node.js?**
    - **Answer:** Streams are an abstraction for handling data that is read or written in chunks, making it more memory efficient. There are four types of streams in Node.js: Readable, Writable, Duplex, and Transform.
    - **Example:**
      ```js
      const fs = require('fs');
      const readableStream = fs.createReadStream('example.txt', 'utf8');
      const writableStream = fs.createWriteStream('output.txt');

      readableStream.pipe(writableStream);  // Pipe data from input file to output file
      ```

---

41. **Explain the concept of `async` and `await` in Node.js.**
    - **Answer:** `async/await` is syntactic sugar over promises, allowing asynchronous code to be written in a more synchronous style.
    - **Example:**
      ```js
      const fetchData = () => {
        return new Promise((resolve) => {
          setTimeout(() => resolve('Data fetched'), 1000);
        });
      };

      const processData = async () => {
        console.log('Start fetching data...');
        const data = await fetchData();  // Await the promise resolution
        console.log(data);  // Output: Data fetched
      };

      processData();
      ```

---

42. **How do you handle errors in Node.js?**
    - **Answer:** You can handle errors in Node.js using `try/catch` blocks for synchronous code or `.catch()` for promises.
    - **Example:**
      ```js
      // Handling synchronous errors
      try {
        const data = JSON.parse('invalid JSON');
      } catch (error) {
        console.error('Error occurred:', error.message);
      }

      // Handling asynchronous errors (Promises)
      const fetchData = new Promise((resolve, reject) => {
        reject('Error: Failed to fetch data');
      });

      fetchData.catch(error => console.error(error));  // Output: Error: Failed to fetch data
      ```

---

43. **What is the `fs` module in Node.js and how can you use it?**
    - **Answer:** The `fs` (File System) module allows you to interact with the file system, such as reading, writing, and manipulating files.
    - **Example:**
      ```js
      const fs = require('fs');

      // Reading a file asynchronously
      fs.readFile('example.txt', 'utf8', (err, data) => {
        if (err) throw err;
        console.log(data);
      });

      // Writing to a file
      fs.writeFile('output.txt', 'Hello, Node.js!', (err) => {
        if (err) throw err;
        console.log('File saved!');
      });
      ```

---

44. **What is a `buffer` in Node.js and how is it used?**
    - **Answer:** Buffers are used to handle raw binary data in Node.js. Buffers are particularly useful when dealing with streams or I/O operations that involve binary data.
    - **Example:**
      ```js
      const buffer = Buffer.from('Hello, Node.js!');
      console.log(buffer);  // Output: <Buffer 48 65 6c 6c 6f 2c 20 4e 6f 64 65 2e 6a 73 21>
      console.log(buffer.toString());  // Output: Hello, Node.js!
      ```

---

45. **What is the `cluster` module in Node.js and how can you use it for load balancing?**
    - **Answer:** The `cluster` module allows you to create child processes (workers) that share server ports, enabling multi-core processors to be used effectively.
    - **Example:**
      ```js
      const cluster = require('cluster');
      const http = require('http');
      const numCPUs = require('os').cpus().length;

      if (cluster.isMaster) {
        // Fork workers
        for (let i = 0; i < numCPUs; i++) {
          cluster.fork();
        }

        cluster.on('exit', (worker, code, signal) => {
          console.log(`Worker ${worker.process.pid} died`);
        });
      } else {
        // Worker processes
        http.createServer((req, res) => {
          res.writeHead(200);
          res.end('Hello World');
        }).listen(8000);
      }
      ```

---

46. **What is the `http` module in Node.js?**
    - **Answer:** The `http` module provides functionality for creating web servers, handling requests, and sending responses.
    - **Example:**
      ```js
      const http = require('http');

      const server = http.createServer((req, res) => {
        res.writeHead(200, { 'Content-Type': 'text/plain' });
        res.end('Hello, Node.js Server!');
      });

      server.listen(3000, () => {
        console.log('Server is running at http://localhost:3000');
      });
      ```

---

47. **What are environment variables in Node.js, and how do you manage them?**
    - **Answer:** Environment variables are used to store configuration settings that can be accessed within your application. You can manage them using the `process.env` object or the `dotenv` package.
    - **Example using `dotenv`:**
      ```js
      require('dotenv').config();

      console.log(process.env.MY_VARIABLE);  // Output: value from .env file
      ```

Here are more Node.js interview questions with examples:

---

### **Advanced Node.js Interview Questions with Code Examples (Continued)**

---

48. **What are the differences between `require()` and `import` in Node.js?**
    - **Answer:** 
      - `require()` is used in CommonJS modules, while `import` is used in ES modules (ECMAScript modules). Node.js started supporting `import` in version 12, and it provides a more standardized way of importing/exporting modules.
      - **Example (CommonJS):**
        ```js
        // CommonJS module (require)
        const fs = require('fs');
        ```
      - **Example (ES Modules):**
        ```js
        // ES module (import)
        import fs from 'fs';
        ```

---

49. **What is `global` in Node.js?**
    - **Answer:** The `global` object provides a way to access global variables, similar to `window` in browsers. It is the top-level scope for variables in Node.js.
    - **Example:**
      ```js
      global.myGlobalVar = 'This is global!';
      console.log(myGlobalVar);  // Output: This is global!
      ```

---

50. **How can you set up a simple REST API in Node.js?**
    - **Answer:** Using Express.js, you can easily set up RESTful routes for creating, reading, updating, and deleting resources.
    - **Example (Simple REST API using Express.js):**
      ```js
      const express = require('express');
      const app = express();
      app.use(express.json());

      let items = [{ id: 1, name: 'Item 1' }];

      // Create
      app.post('/items', (req, res) => {
        const newItem = req.body;
        newItem.id = items.length + 1;
        items.push(newItem);
        res.status(201).send(newItem);
      });

      // Read
      app.get('/items', (req, res) => {
        res.status(200).send(items);
      });

      // Update
      app.put('/items/:id', (req, res) => {
        const itemId = parseInt(req.params.id);
        const updatedItem = req.body;
        const index = items.findIndex(item => item.id === itemId);
        if (index !== -1) {
          items[index] = updatedItem;
          res.status(200).send(updatedItem);
        } else {
          res.status(404).send({ message: 'Item not found' });
        }
      });

      // Delete
      app.delete('/items/:id', (req, res) => {
        const itemId = parseInt(req.params.id);
        items = items.filter(item => item.id !== itemId);
        res.status(204).send();
      });

      app.listen(3000, () => console.log('Server running on port 3000'));
      ```

---

51. **What is the purpose of `process.env` in Node.js?**
    - **Answer:** `process.env` is used to access environment variables, which can be set outside the application (in the shell, for example) to store configuration settings.
    - **Example:**
      ```js
      console.log(process.env.NODE_ENV);  // Output: production (if set in the environment)
      ```

---

52. **How do you handle asynchronous functions that may throw errors in Node.js?**
    - **Answer:** You can handle errors in asynchronous functions using `try/catch` within `async` functions, or `.catch()` for promises.
    - **Example:**
      ```js
      const fetchData = async () => {
        try {
          const data = await someAsyncFunction();
          console.log(data);
        } catch (error) {
          console.error('Error fetching data:', error);
        }
      };

      fetchData();
      ```

---

53. **How do you manage large file uploads in Node.js?**
    - **Answer:** You can use libraries like `multer` to handle large file uploads in Node.js. `multer` allows you to handle `multipart/form-data` and manage file storage.
    - **Example (using `multer` for file upload):**
      ```js
      const express = require('express');
      const multer = require('multer');
      const app = express();
      const upload = multer({ dest: 'uploads/' });

      app.post('/upload', upload.single('file'), (req, res) => {
        console.log(req.file);  // File metadata
        res.send('File uploaded successfully!');
      });

      app.listen(3000, () => console.log('Server running on port 3000'));
      ```

---

54. **What is the `querystring` module in Node.js?**
    - **Answer:** The `querystring` module provides utilities for parsing and formatting query strings in URLs.
    - **Example:**
      ```js
      const querystring = require('querystring');

      const parsedQuery = querystring.parse('name=John&age=30');
      console.log(parsedQuery);  // Output: { name: 'John', age: '30' }

      const queryString = querystring.stringify({ name: 'John', age: 30 });
      console.log(queryString);  // Output: name=John&age=30
      ```

---

55. **What is `pm2` and how can it be used in Node.js?**
    - **Answer:** `pm2` is a process manager for Node.js applications. It helps in managing, monitoring, and keeping applications alive forever.
    - **Example:**
      1. Install `pm2` globally: 
         ```bash
         npm install pm2 -g
         ```
      2. Start your Node.js application with `pm2`:
         ```bash
         pm2 start app.js
         ```

---

56. **What is `cors` and why is it used in Node.js applications?**
    - **Answer:** `cors` (Cross-Origin Resource Sharing) is a middleware used to allow or restrict requested resources on a web server depending on the origin of the request. It's commonly used to handle cross-origin requests in web applications.
    - **Example (using `cors` in Express.js):**
      ```js
      const express = require('express');
      const cors = require('cors');
      const app = express();

      app.use(cors());  // Allow all origins by default

      app.get('/data', (req, res) => {
        res.json({ message: 'This is CORS-enabled for all origins!' });
      });

      app.listen(3000, () => console.log('Server running on port 3000'));
      ```

---

57. **How do you create a WebSocket server in Node.js?**
    - **Answer:** You can create a WebSocket server in Node.js using the `ws` library, which provides an easy-to-use API for handling WebSocket connections.
    - **Example:**
      ```js
      const WebSocket = require('ws');
      const wss = new WebSocket.Server({ port: 8080 });

      wss.on('connection', (ws) => {
        console.log('New client connected');
        ws.on('message', (message) => {
          console.log(`Received message: ${message}`);
          ws.send('Hello from the server');
        });
      });

      console.log('WebSocket server running on ws://localhost:8080');
      ```

---

58. **What is the role of `next()` in Express.js middleware?**
    - **Answer:** `next()` is a function that is called within a middleware function to pass control to the next middleware in the stack. If `next()` is not called, the request-response cycle will hang.
    - **Example:**
      ```js
      const express = require('express');
      const app = express();

      app.use((req, res, next) => {
        console.log('Middleware 1');
        next();  // Pass control to the next middleware
      });

      app.use((req, res, next) => {
        console.log('Middleware 2');
        res.send('Response from Middleware 2');
      });

      app.listen(3000, () => console.log('Server running on port 3000'));
      ```

---

59. **How do you handle rate limiting in Node.js?**
    - **Answer:** You can implement rate limiting using the `express-rate-limit` library. This helps prevent abuse of your API by limiting the number of requests a client can make in a given time period.
    - **Example:**
      ```js
      const express = require('express');
      const rateLimit = require('express-rate-limit');
      const app = express();

      const limiter = rateLimit({
        windowMs: 15 * 60 * 1000,  // 15 minutes
        max: 100,  // Limit each IP to 100 requests per windowMs
        message: 'Too many requests, please try again later.'
      });

      app.use(limiter);

      app.get('/', (req, res) => {
        res.send('Hello World');
      });

      app.listen(3000, () => console.log('Server running on port 3000'));
      ```

---

60. **What is `helmet` in Node.js, and why should you use it?**
    - **Answer:** `helmet` is a middleware used to secure Express.js applications by setting various HTTP headers that help protect against common security threats like clickjacking, cross-site scripting (XSS), and others.
    - **Example:**
      ```js
      const express = require('express');
      const helmet = require('helmet');
      const app = express();

      app.use(helmet());  // Enable all Helmet security features

      app.get('/', (req, res) => {
        res.send('Hello, secure world!');
      });

      app.listen(3000, () => console.log('Server running on port 3000'));
      ```

Here are more Node.js interview questions with explanations and code examples:

---

### **Advanced Node.js Interview Questions with Code Examples (Continued)**

---

61. **What is the `dns` module in Node.js?**
    - **Answer:** The `dns` module provides a way to perform DNS lookups and resolve domain names into IP addresses.
    - **Example:**
      ```js
      const dns = require('dns');

      dns.lookup('google.com', (err, address, family) => {
        if (err) throw err;
        console.log('Address: %j Family: IPv' + family, address);
      });
      ```

---

62. **What is the `util` module in Node.js?**
    - **Answer:** The `util` module provides various utility functions, such as inspecting objects, formatting strings, and promoting functions.
    - **Example:**
      ```js
      const util = require('util');

      // Using util.format
      const name = 'John';
      const greeting = util.format('Hello, %s!', name);
      console.log(greeting);  // Output: Hello, John!

      // Using util.inspect
      const obj = { name: 'John', age: 30 };
      console.log(util.inspect(obj));  // Output: { name: 'John', age: 30 }
      ```

---

63. **What is the `path` module in Node.js?**
    - **Answer:** The `path` module provides utilities for working with file and directory paths, such as joining, resolving, or normalizing paths.
    - **Example:**
      ```js
      const path = require('path');

      const filePath = '/home/user/website/index.html';
      const dirName = path.dirname(filePath);
      const baseName = path.basename(filePath);
      const extName = path.extname(filePath);

      console.log('Directory:', dirName);  // Output: /home/user/website
      console.log('File name:', baseName);  // Output: index.html
      console.log('Extension:', extName);  // Output: .html
      ```

---

64. **How do you perform database operations with Node.js?**
    - **Answer:** You can interact with databases (e.g., MySQL, MongoDB) using libraries like `mysql2` or `mongoose` for MongoDB. 
    - **Example (MySQL):**
      ```js
      const mysql = require('mysql2');

      const connection = mysql.createConnection({
        host: 'localhost',
        user: 'root',
        database: 'test'
      });

      connection.query('SELECT * FROM users', (err, results) => {
        if (err) throw err;
        console.log(results);
      });

      connection.end();
      ```

    - **Example (MongoDB using Mongoose):**
      ```js
      const mongoose = require('mongoose');
      mongoose.connect('mongodb://localhost/test', { useNewUrlParser: true, useUnifiedTopology: true });

      const User = mongoose.model('User', new mongoose.Schema({ name: String, age: Number }));

      const user = new User({ name: 'John', age: 30 });
      user.save().then(() => console.log('User saved!'));
      ```

---

65. **What is the `assert` module in Node.js?**
    - **Answer:** The `assert` module is used for writing tests and making assertions in your code. It helps verify that the code is functioning correctly.
    - **Example:**
      ```js
      const assert = require('assert');

      assert.strictEqual(2 + 2, 4);  // Passes
      assert.strictEqual(2 + 2, 5);  // Throws AssertionError: 2 + 2 == 5
      ```

---

66. **What is the `process` object in Node.js?**
    - **Answer:** The `process` object is a global object that provides information about the current Node.js process, such as environment variables, command-line arguments, and methods to terminate the process.
    - **Example:**
      ```js
      console.log('Node version:', process.version);  // Output: Node version: v14.x.x
      console.log('Arguments:', process.argv);  // Output: Arguments: [ 'node', 'app.js', 'arg1', 'arg2' ]
      ```

---

67. **What are worker threads in Node.js?**
    - **Answer:** Worker threads in Node.js allow you to run JavaScript code in parallel on multiple threads, making it easier to handle CPU-intensive tasks.
    - **Example:**
      ```js
      const { Worker, isMainThread, parentPort } = require('worker_threads');

      if (isMainThread) {
        const worker = new Worker(__filename);
        worker.on('message', (message) => console.log(message));
        worker.postMessage('Hello from main thread');
      } else {
        parentPort.on('message', (message) => {
          console.log(message);  // Output: Hello from main thread
          parentPort.postMessage('Hello from worker thread');
        });
      }
      ```

---

68. **What is the difference between `__dirname` and `__filename`?**
    - **Answer:** 
      - `__dirname` gives the directory name of the current module (file).
      - `__filename` gives the full path of the current module (file).
    - **Example:**
      ```js
      console.log('__dirname:', __dirname);  // Output: Path to the current directory
      console.log('__filename:', __filename);  // Output: Full file path of the current module
      ```

---

69. **What is the difference between `setImmediate()` and `setTimeout()` in Node.js?**
    - **Answer:** 
      - `setImmediate()` schedules a callback to be executed after the current event loop cycle.
      - `setTimeout()` schedules a callback to be executed after a specified time delay.
    - **Example:**
      ```js
      setImmediate(() => {
        console.log('Executed immediately after the current event loop cycle');
      });

      setTimeout(() => {
        console.log('Executed after 0 milliseconds');
      }, 0);
      ```

---

70. **How do you handle JSON data in Node.js?**
    - **Answer:** You can use `JSON.parse()` to parse JSON strings into objects and `JSON.stringify()` to convert objects into JSON strings.
    - **Example:**
      ```js
      const jsonString = '{"name": "John", "age": 30}';
      const parsedObj = JSON.parse(jsonString);
      console.log(parsedObj);  // Output: { name: 'John', age: 30 }

      const jsonStringified = JSON.stringify(parsedObj);
      console.log(jsonStringified);  // Output: {"name":"John","age":30}
      ```

---

71. **How can you optimize performance in a Node.js application?**
    - **Answer:** There are several ways to optimize performance:
      - Use asynchronous and non-blocking I/O operations.
      - Use clustering for handling multiple CPU cores.
      - Use caching mechanisms like Redis.
      - Profile your code and identify performance bottlenecks using tools like `Node.js profiler` or `clinic.js`.
      - Example of clustering:
        ```js
        const cluster = require('cluster');
        const http = require('http');
        const os = require('os');
        const numCPUs = os.cpus().length;

        if (cluster.isMaster) {
          // Fork workers.
          for (let i = 0; i < numCPUs; i++) {
            cluster.fork();
          }
        } else {
          // Workers can share the same server port.
          http.createServer((req, res) => {
            res.writeHead(200);
            res.end('Hello World');
          }).listen(8000);
        }
        ```

---

72. **What are the differences between Node.js and traditional server-side programming languages (e.g., PHP, Java)?**
    - **Answer:** 
      - Node.js is event-driven and non-blocking, making it ideal for handling high-concurrency applications, such as chat applications and real-time systems.
      - Traditional server-side languages like PHP and Java are generally synchronous and block the execution thread while handling requests, which may result in slower response times under heavy load.
    - **Key Advantages of Node.js:**
      - Single-threaded, non-blocking, event-driven model.
      - Uses JavaScript (familiar for frontend developers).
      - Well-suited for I/O-heavy operations.
      - Highly scalable with event loops.

---

73. **What is the `stream` module in Node.js?**
    - **Answer:** The `stream` module provides APIs for working with streaming data, such as reading files, HTTP requests, or writing data to files. It allows you to handle large amounts of data efficiently by processing it in chunks.
    - **Example (Readable Stream):**
      ```js
      const fs = require('fs');
      const readableStream = fs.createReadStream('largefile.txt');

      readableStream.on('data', (chunk) => {
        console.log('Received chunk:', chunk);
      });

      readableStream.on('end', () => {
        console.log('Stream finished');
      });
      ```
Here are more Node.js interview questions with explanations and code examples:

---

### **Advanced Node.js Interview Questions with Code Examples (Continued)**

---

74. **What is `EventEmitter` in Node.js?**
    - **Answer:** `EventEmitter` is a class in Node.js that allows objects to emit events and other objects to listen for and handle these events. It's a core part of the event-driven architecture in Node.js.
    - **Example:**
      ```js
      const EventEmitter = require('events');
      const emitter = new EventEmitter();

      // Register event listener
      emitter.on('greet', () => {
        console.log('Hello, world!');
      });

      // Emit event
      emitter.emit('greet');  // Output: Hello, world!
      ```

---

75. **What is the purpose of the `nextTick()` function in Node.js?**
    - **Answer:** `process.nextTick()` is used to defer the execution of a function to the next phase of the event loop. It is often used to ensure that a callback is executed before any I/O events in the event loop.
    - **Example:**
      ```js
      console.log('Start');
      
      process.nextTick(() => {
        console.log('Executed in next tick');
      });

      console.log('End');
      // Output:
      // Start
      // End
      // Executed in next tick
      ```

---

76. **What is the purpose of `setTimeout()` and `setInterval()` in Node.js?**
    - **Answer:** 
      - `setTimeout()` is used to schedule a one-time execution of a function after a delay.
      - `setInterval()` is used to repeatedly execute a function at specified intervals.
    - **Example:**
      ```js
      // setTimeout Example
      setTimeout(() => {
        console.log('This message is shown after 2 seconds');
      }, 2000);

      // setInterval Example
      let counter = 0;
      const interval = setInterval(() => {
        console.log('This message is shown every 1 second');
        counter++;
        if (counter === 3) {
          clearInterval(interval);
        }
      }, 1000);
      ```

---

77. **How do you implement logging in a Node.js application?**
    - **Answer:** You can use the built-in `console` object or third-party libraries like `winston` or `morgan` for logging in Node.js applications.
    - **Example (using `winston` for logging):**
      ```js
      const winston = require('winston');

      const logger = winston.createLogger({
        level: 'info',
        format: winston.format.simple(),
        transports: [
          new winston.transports.Console()
        ],
      });

      logger.info('This is an info message');
      logger.error('This is an error message');
      ```

---

78. **What are Streams in Node.js and how do they work?**
    - **Answer:** Streams are objects that allow you to read data from a source or write data to a destination in a continuous manner. There are four types of streams in Node.js:
      - Readable
      - Writable
      - Duplex
      - Transform
    - **Example (Readable Stream):**
      ```js
      const fs = require('fs');
      const readableStream = fs.createReadStream('sample.txt', 'utf8');

      readableStream.on('data', (chunk) => {
        console.log('Received chunk:', chunk);
      });

      readableStream.on('end', () => {
        console.log('Stream finished');
      });
      ```

---

79. **What are Promises in Node.js and how do they differ from callbacks?**
    - **Answer:** Promises are a way of handling asynchronous operations and can help avoid "callback hell." A Promise represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
    - **Example:**
      ```js
      const someAsyncFunction = () => {
        return new Promise((resolve, reject) => {
          setTimeout(() => {
            resolve('Success!');
          }, 2000);
        });
      };

      someAsyncFunction()
        .then(result => console.log(result))  // Output: Success!
        .catch(error => console.error(error));
      ```

---

80. **What are async/await in Node.js?**
    - **Answer:** `async` and `await` are syntactic sugar built on top of Promises to make asynchronous code easier to write and read. `async` is used to define a function as asynchronous, and `await` pauses the execution until the Promise is resolved or rejected.
    - **Example:**
      ```js
      const fetchData = async () => {
        const data = await someAsyncFunction();
        console.log(data);
      };

      fetchData();
      ```

---

81. **How can you handle HTTP requests in Node.js?**
    - **Answer:** You can handle HTTP requests using the built-in `http` module or by using a web framework like Express.js.
    - **Example (Using the `http` module):**
      ```js
      const http = require('http');

      const server = http.createServer((req, res) => {
        res.writeHead(200, { 'Content-Type': 'text/plain' });
        res.end('Hello, World!');
      });

      server.listen(3000, () => {
        console.log('Server is running on port 3000');
      });
      ```

    - **Example (Using Express.js):**
      ```js
      const express = require('express');
      const app = express();

      app.get('/', (req, res) => {
        res.send('Hello, World!');
      });

      app.listen(3000, () => {
        console.log('Server is running on port 3000');
      });
      ```

---

82. **What is `node-fetch` and how do you use it in Node.js?**
    - **Answer:** `node-fetch` is a lightweight module for making HTTP requests, similar to the `fetch` API available in browsers. It is often used to interact with RESTful APIs in Node.js.
    - **Example:**
      ```js
      const fetch = require('node-fetch');

      fetch('https://jsonplaceholder.typicode.com/posts')
        .then(response => response.json())
        .then(data => console.log(data))
        .catch(error => console.error('Error:', error));
      ```

---

83. **How do you manage environment variables in a Node.js project?**
    - **Answer:** You can use the `dotenv` library to manage environment variables in Node.js. This library loads environment variables from a `.env` file into `process.env`.
    - **Example:**
      1. Install `dotenv`:
         ```bash
         npm install dotenv
         ```

      2. Create a `.env` file:
         ```
         DB_HOST=localhost
         DB_USER=root
         DB_PASS=password
         ```

      3. Load the environment variables in your code:
         ```js
         require('dotenv').config();

         console.log(process.env.DB_HOST);  // Output: localhost
         console.log(process.env.DB_USER);  // Output: root
         console.log(process.env.DB_PASS);  // Output: password
         ```

---

84. **What are the differences between `fs.readFile()` and `fs.createReadStream()` in Node.js?**
    - **Answer:** 
      - `fs.readFile()` reads the entire file into memory, which can be inefficient for large files.
      - `fs.createReadStream()` creates a stream for reading a file, allowing you to process data as it is being read (useful for large files).
    - **Example (fs.readFile):**
      ```js
      const fs = require('fs');

      fs.readFile('largefile.txt', 'utf8', (err, data) => {
        if (err) throw err;
        console.log(data);
      });
      ```

    - **Example (fs.createReadStream):**
      ```js
      const fs = require('fs');

      const readableStream = fs.createReadStream('largefile.txt', 'utf8');

      readableStream.on('data', (chunk) => {
        console.log('Received chunk:', chunk);
      });
      ```

---

85. **How do you handle authentication in a Node.js application?**
    - **Answer:** You can handle authentication using various strategies like JWT (JSON Web Tokens), session-based authentication, or third-party libraries like Passport.js.
    - **Example (Using JWT):**
      ```js
      const jwt = require('jsonwebtoken');
      const express = require('express');
      const app = express();
      const secretKey = 'your-secret-key';

      // Middleware to authenticate JWT
      const authenticateToken = (req, res, next) => {
        const token = req.header('Authorization');
        if (!token) return res.sendStatus(401);
        jwt.verify(token, secretKey, (err, user) => {
          if (err) return res.sendStatus(403);
          req.user = user;
          next();
        });
      };

      // Login route
      app.post('/login', (req, res) => {
        const username = req.body.username;
        const token = jwt.sign({ username }, secretKey);
        res.json({ token });
      });

      // Protected route
      app.get('/protected', authenticateToken, (req, res) => {
        res.send('This is a protected route');
      });

      app.listen(3000, () => console.log('Server running on port 3000'));
      ```

---

86. **How can you test a Node.js application?**
    - **Answer:** You can use testing frameworks like Mocha, Jasmine, or Jest to test your Node.js application. These frameworks help you write unit and integration tests.
    - **Example (Using Mocha and Chai for testing):**
      ```js
      const assert = require('chai').assert;

      describe('Array', function () {
        it('should start empty', function () {
          let arr = [];
          assert.equal(arr.length, 0);
        });
      });
      ```

Here are more advanced Node.js interview questions with explanations and code examples:

---

### **Advanced Node.js Interview Questions with Code Examples (Continued)**

---

87. **What are `cluster` and `worker threads` in Node.js, and how do they differ?**
    - **Answer:**
      - **`cluster`**: Used to create multiple instances of a Node.js application to utilize multi-core systems and improve performance by distributing incoming requests across workers.
      - **`worker threads`**: Provides a way to execute JavaScript in parallel threads. These threads run independently but share memory via the `SharedArrayBuffer` API.
    - **Example (Cluster):**
      ```js
      const cluster = require('cluster');
      const http = require('http');
      const os = require('os');
      const numCPUs = os.cpus().length;

      if (cluster.isMaster) {
        // Fork workers
        for (let i = 0; i < numCPUs; i++) {
          cluster.fork();
        }
      } else {
        http.createServer((req, res) => {
          res.writeHead(200, { 'Content-Type': 'text/plain' });
          res.end('Hello, World!');
        }).listen(3000);
      }
      ```

    - **Example (Worker Threads):**
      ```js
      const { Worker, isMainThread, parentPort } = require('worker_threads');

      if (isMainThread) {
        const worker = new Worker(__filename);
        worker.on('message', (message) => console.log(message));
        worker.postMessage('Hello from main thread');
      } else {
        parentPort.on('message', (message) => {
          console.log(message);  // Output: Hello from main thread
          parentPort.postMessage('Hello from worker thread');
        });
      }
      ```

---

88. **What is the Event Loop in Node.js and how does it work?**
    - **Answer:** The Event Loop is a mechanism that allows Node.js to handle asynchronous operations in a non-blocking manner. The event loop runs continuously, handling callbacks, I/O operations, and executing code that is ready to run.
    - **Stages of the Event Loop**:
      1. **Timers** - `setTimeout` and `setInterval`
      2. **Pending Callbacks** - I/O callbacks, e.g., TCP callbacks
      3. **Idle, prepare** - Internal operations
      4. **Poll** - Handles incoming events
      5. **Check** - Runs `setImmediate` callbacks
      6. **Close callbacks** - e.g., `socket.on('close')`
    - **Example:**
      ```js
      console.log('Start');

      setTimeout(() => {
        console.log('Timeout');
      }, 0);

      setImmediate(() => {
        console.log('Immediate');
      });

      console.log('End');

      // Output:
      // Start
      // End
      // Immediate
      // Timeout
      ```

---

89. **How can you debug a Node.js application?**
    - **Answer:** You can debug Node.js applications using:
      - The `--inspect` flag (enables debugging via Chrome DevTools).
      - The `debugger` keyword (pauses code execution at a specified point).
      - Console logging.
    - **Example (Using the `--inspect` flag):**
      ```bash
      node --inspect app.js
      ```
      Open Chrome DevTools and navigate to `chrome://inspect` to start debugging.

      **Example (Using `debugger`):**
      ```js
      function calculate(a, b) {
        debugger;  // Pauses execution
        return a + b;
      }

      calculate(2, 3);
      ```

---

90. **How can you manage large-scale configurations in Node.js applications?**
    - **Answer:** For managing configurations, you can use tools like `dotenv` to load environment variables from a `.env` file or use external services like AWS Systems Manager Parameter Store, HashiCorp Vault, or Kubernetes ConfigMaps for managing configurations in production.
    - **Example (Using `dotenv`):**
      1. Install `dotenv`:
         ```bash
         npm install dotenv
         ```
      2. Create a `.env` file:
         ```
         DB_HOST=localhost
         DB_USER=root
         DB_PASS=password
         ```
      3. Load environment variables:
         ```js
         require('dotenv').config();

         console.log(process.env.DB_HOST);  // Output: localhost
         ```

---

91. **What are middleware functions in Express.js?**
    - **Answer:** Middleware functions are functions that have access to the request (`req`), response (`res`), and the next middleware function in the request-response cycle. They are used for tasks like logging, authentication, request parsing, etc.
    - **Example:**
      ```js
      const express = require('express');
      const app = express();

      // Custom middleware to log the request
      app.use((req, res, next) => {
        console.log('Request URL:', req.url);
        next();  // Pass control to the next middleware
      });

      app.get('/', (req, res) => {
        res.send('Hello, World!');
      });

      app.listen(3000, () => {
        console.log('Server running on port 3000');
      });
      ```

---

92. **How do you handle file uploads in Node.js?**
    - **Answer:** File uploads in Node.js are typically handled using libraries like `multer`. This library handles multipart form-data and makes it easier to handle file uploads.
    - **Example (Using `multer`):**
      1. Install `multer`:
         ```bash
         npm install multer
         ```
      2. Create a basic file upload endpoint:
         ```js
         const express = require('express');
         const multer = require('multer');
         const upload = multer({ dest: 'uploads/' });
         const app = express();

         app.post('/upload', upload.single('file'), (req, res) => {
           console.log(req.file);  // File information
           res.send('File uploaded successfully!');
         });

         app.listen(3000, () => {
           console.log('Server running on port 3000');
         });
         ```

---

93. **What is the `Buffer` class in Node.js?**
    - **Answer:** The `Buffer` class is used to handle binary data. It is particularly useful for working with raw binary data, such as reading files, interacting with streams, and handling TCP connections.
    - **Example:**
      ```js
      const buffer = Buffer.from('Hello, World!', 'utf8');
      console.log(buffer);  // Output: <Buffer 48 65 6c 6c 6f 2c 20 57 6f 72 6c 64 21>
      ```

---

94. **What is the purpose of `req.body`, `req.params`, and `req.query` in Express.js?**
    - **Answer:**
      - `req.body` contains data sent in the body of a POST or PUT request (useful when handling form submissions or JSON data).
      - `req.params` contains route parameters in the URL.
      - `req.query` contains query parameters in the URL.
    - **Example:**
      ```js
      const express = require('express');
      const app = express();

      // Parsing JSON bodies
      app.use(express.json());

      // Handling POST request
      app.post('/user', (req, res) => {
        console.log(req.body);  // { name: 'John', age: 30 }
        res.send('User data received');
      });

      // Handling route parameters
      app.get('/user/:id', (req, res) => {
        console.log(req.params.id);  // User ID from the URL
        res.send('User data');
      });

      // Handling query parameters
      app.get('/search', (req, res) => {
        console.log(req.query.q);  // Query parameter 'q'
        res.send('Search results');
      });

      app.listen(3000, () => {
        console.log('Server running on port 3000');
      });
      ```

---

95. **What is `npm run` and how is it used in Node.js?**
    - **Answer:** `npm run` is used to execute custom scripts defined in the `package.json` file. It allows you to run build commands, test commands, or any other script.
    - **Example (package.json):**
      ```json
      {
        "scripts": {
          "start": "node app.js",
          "test": "mocha test.js"
        }
      }
      ```

      You can run these scripts using:
      ```bash
      npm run start
      npm run test
      ```

---

96. **How do you implement rate limiting in a Node.js application?**
    - **Answer:** You can implement rate limiting using middleware like `express-rate-limit` to prevent excessive requests to your API and protect your server from abuse.
    - **Example (Using `express-rate-limit`):**
      1. Install `express-rate-limit`:
         ```bash
         npm install express-rate-limit
         ```
      2. Implement rate limiting:
         ```js
         const express = require('express');
         const rateLimit = require('express-rate-limit');
         const app = express();

         const limiter = rateLimit({
           windowMs: 15 * 60 * 1000,  // 15 minutes
           max: 100  // Limit each IP to 100 requests per windowMs
         });

         app.use(limiter);

         app.get('/', (req, res) => {
           res.send('Hello, World!');
         });

         app.listen(3000, () => {
           console.log('Server running on port 3000');
         });
         ```

Here are even more advanced Node.js interview questions with explanations and code examples:

---

### **Advanced Node.js Interview Questions with Code Examples (Continued)**

---

97. **What is `Node.js`'s `child_process` module, and how can you use it?**
    - **Answer:** The `child_process` module allows you to spawn child processes in Node.js. This can be useful for running shell commands, scripts, or external processes without blocking the main thread.
    - **Example:**
      ```js
      const { exec } = require('child_process');

      exec('ls -l', (err, stdout, stderr) => {
        if (err) {
          console.error(`Error: ${err}`);
          return;
        }
        console.log(`Output: ${stdout}`);
        console.error(`Errors: ${stderr}`);
      });
      ```

    - **Example (Using `spawn`):**
      ```js
      const { spawn } = require('child_process');
      const ls = spawn('ls', ['-lh', '/usr']);

      ls.stdout.on('data', (data) => {
        console.log(`stdout: ${data}`);
      });

      ls.stderr.on('data', (data) => {
        console.error(`stderr: ${data}`);
      });

      ls.on('close', (code) => {
        console.log(`child process exited with code ${code}`);
      });
      ```

---

98. **What is the `Buffer` class in Node.js, and how do you use it?**
    - **Answer:** The `Buffer` class is used to handle raw binary data directly in Node.js. Buffers are useful when working with I/O operations like reading files or interacting with streams.
    - **Example:**
      ```js
      const buffer = Buffer.from('Hello World!', 'utf8');
      console.log(buffer);  // Output: <Buffer 48 65 6c 6c 6f 20 57 6f 72 6c 64 21>
      ```

      You can also manipulate individual bytes in the buffer:
      ```js
      const buffer = Buffer.alloc(4);
      buffer.writeUInt8(10, 0);
      buffer.writeUInt8(20, 1);
      console.log(buffer);  // Output: <Buffer 0a 14 00 00>
      ```

---

99. **What are `global` objects in Node.js, and how do they work?**
    - **Answer:** `global` objects in Node.js are objects that are globally available across the entire application. Some commonly used global objects include `__dirname`, `__filename`, `process`, and `console`.
    - **Example:**
      ```js
      console.log(__dirname);  // Current directory
      console.log(__filename); // Current file path

      process.exit(0);  // Exit the application
      ```

---

100. **What is the purpose of `path` module in Node.js?**
    - **Answer:** The `path` module in Node.js provides utilities for working with file and directory paths. It helps to manipulate file paths in a way that works across different operating systems.
    - **Example:**
      ```js
      const path = require('path');

      const filePath = '/Users/sandeep/myapp/index.js';

      console.log(path.basename(filePath));  // Output: index.js
      console.log(path.dirname(filePath));   // Output: /Users/sandeep/myapp
      console.log(path.extname(filePath));   // Output: .js
      ```

---

101. **What are `promisify` and `async/await`? How are they related?**
    - **Answer:** `promisify` is a utility in Node.js (via the `util` module) that converts callback-based functions into functions that return Promises. `async/await` is a syntax sugar for handling asynchronous operations that makes code look synchronous.
    - **Example (Using `promisify`):**
      ```js
      const fs = require('fs');
      const { promisify } = require('util');
      const readFile = promisify(fs.readFile);

      (async () => {
        try {
          const data = await readFile('example.txt', 'utf8');
          console.log(data);
        } catch (err) {
          console.error(err);
        }
      })();
      ```

---

102. **What is the `EventEmitter` class, and how can you use it?**
    - **Answer:** The `EventEmitter` class in Node.js allows objects to emit events and other objects to listen and respond to those events. It is widely used for building event-driven architectures.
    - **Example:**
      ```js
      const EventEmitter = require('events');
      const emitter = new EventEmitter();

      emitter.on('message', (message) => {
        console.log('Received message:', message);
      });

      emitter.emit('message', 'Hello, Node.js!');
      ```

---

103. **What is `Express.js`, and why should you use it in a Node.js application?**
    - **Answer:** Express.js is a minimalist web framework for Node.js, which simplifies building web applications and APIs. It provides middleware, routing, and utility functions to make handling HTTP requests easier.
    - **Example:**
      ```js
      const express = require('express');
      const app = express();

      app.get('/', (req, res) => {
        res.send('Hello, Express!');
      });

      app.listen(3000, () => {
        console.log('Server running on port 3000');
      });
      ```

---

104. **What are `setImmediate()` and `setTimeout()` in Node.js, and how do they differ?**
    - **Answer:**
      - `setTimeout()` is used to schedule a one-time execution of a function after a specified delay.
      - `setImmediate()` is used to schedule a callback to execute in the next iteration of the event loop, after I/O events.
    - **Example:**
      ```js
      setTimeout(() => {
        console.log('This is executed after 0 ms');
      }, 0);

      setImmediate(() => {
        console.log('This is executed in the next event loop iteration');
      });

      console.log('This is executed first');
      ```

      **Output:**
      ```
      This is executed first
      This is executed in the next event loop iteration
      This is executed after 0 ms
      ```

---

105. **What is the purpose of the `util` module in Node.js?**
    - **Answer:** The `util` module provides utility functions that help with debugging, formatting, and other common tasks. It includes functions like `promisify`, `inspect`, `format`, and `deprecate`.
    - **Example:**
      ```js
      const util = require('util');

      const format = util.format('Hello, %s!', 'Node.js');
      console.log(format);  // Output: Hello, Node.js!

      // Inspecting objects
      const obj = { name: 'Node.js', version: '16.x' };
      console.log(util.inspect(obj));  // Output: { name: 'Node.js', version: '16.x' }
      ```

---

106. **How do you prevent callback hell in Node.js?**
    - **Answer:** To avoid callback hell, you can:
      1. Use **Promised-based** APIs or libraries like `Promise`, `async/await`.
      2. Refactor the code into smaller functions.
      3. Use libraries such as **Async.js** to manage control flow.
    - **Example (Using `async/await`):**
      ```js
      const fetchData = async () => {
        try {
          const data1 = await fetchDataFromDb();
          const data2 = await fetchDataFromApi(data1);
          console.log(data2);
        } catch (err) {
          console.error(err);
        }
      };

      fetchData();
      ```

---

107. **What are `stream` objects in Node.js?**
    - **Answer:** Streams are objects in Node.js that allow reading or writing data in a continuous flow, enabling efficient handling of large amounts of data. There are four types of streams in Node.js:
      - **Readable**: Used for reading data.
      - **Writable**: Used for writing data.
      - **Duplex**: Can be both readable and writable.
      - **Transform**: A type of duplex stream that can modify data as it is read or written.
    - **Example (Readable Stream):**
      ```js
      const fs = require('fs');
      const readStream = fs.createReadStream('largefile.txt', 'utf8');

      readStream.on('data', (chunk) => {
        console.log('Chunk:', chunk);
      });
      ```

---

108. **What is the purpose of `node_modules` folder in Node.js?**
    - **Answer:** The `node_modules` folder contains all the dependencies required for your Node.js application. These dependencies are specified in the `package.json` file. When you install packages using `npm install`, they are stored in the `node_modules` directory.
    - **Example:**
      - `npm install express` will install the `express` package and its dependencies into the `node_modules` directory.

---

109. **What is the use of `npm install --save` and `npm install --save-dev`?**
    - **Answer:**
      - `--save`: Adds the dependency to the `dependencies` section of `package.json`, indicating that it is needed for production.
      - `--save-dev`: Adds the dependency to the `devDependencies` section of `package.json`, indicating that it is only needed during development.
    - **Example:**
      ```bash
      npm install lodash --save       # Adds to dependencies
      npm install mocha --save-dev    # Adds to devDependencies
      ```

Here are some examples of JavaScript and Node.js logic and programs that showcase fundamental to advanced concepts. These examples are practical and can be extended to real-world applications.

---

### 1. **Basic Logic: Palindrome Check**
```javascript
function isPalindrome(str) {
    const reversed = str.split('').reverse().join('');
    return str === reversed;
}

console.log(isPalindrome("radar")); // true
console.log(isPalindrome("hello")); // false
```

---

### 2. **Node.js HTTP Server**
```javascript
const http = require('http');

const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Hello, World!');
});

server.listen(3000, () => {
    console.log('Server running at http://localhost:3000/');
});
```

---

### 3. **CRUD Operations with Node.js File System (fs)**
```javascript
const fs = require('fs');

// Create
fs.writeFileSync('example.txt', 'This is an example file');

// Read
const content = fs.readFileSync('example.txt', 'utf-8');
console.log(content);

// Update
fs.appendFileSync('example.txt', '\nAppended text');

// Delete
fs.unlinkSync('example.txt');
console.log('File deleted');
```

---

### 4. **Asynchronous Logic: Fetch Data Using Promises**
```javascript
const fetch = require('node-fetch');

async function fetchData(url) {
    try {
        const response = await fetch(url);
        const data = await response.json();
        console.log(data);
    } catch (error) {
        console.error('Error fetching data:', error);
    }
}

fetchData('https://jsonplaceholder.typicode.com/posts/1');
```

---

### 5. **REST API with Express**
```javascript
const express = require('express');
const app = express();

app.use(express.json());

let books = [
    { id: 1, title: 'Book 1' },
    { id: 2, title: 'Book 2' },
];

// Get all books
app.get('/books', (req, res) => {
    res.json(books);
});

// Add a book
app.post('/books', (req, res) => {
    const book = req.body;
    books.push(book);
    res.status(201).json(book);
});

// Update a book
app.put('/books/:id', (req, res) => {
    const id = parseInt(req.params.id);
    const updatedBook = req.body;
    books = books.map(book => (book.id === id ? updatedBook : book));
    res.json(updatedBook);
});

// Delete a book
app.delete('/books/:id', (req, res) => {
    const id = parseInt(req.params.id);
    books = books.filter(book => book.id !== id);
    res.status(204).send();
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 6. **JWT Authentication in Node.js**
```javascript
const jwt = require('jsonwebtoken');

const secretKey = 'mysecretkey';

// Generate Token
function generateToken(user) {
    return jwt.sign(user, secretKey, { expiresIn: '1h' });
}

// Verify Token
function verifyToken(token) {
    try {
        const decoded = jwt.verify(token, secretKey);
        console.log('Verified:', decoded);
    } catch (err) {
        console.error('Invalid token');
    }
}

// Example Usage
const user = { id: 1, username: 'sandeep' };
const token = generateToken(user);
console.log('Token:', token);

verifyToken(token);
```

---

### 7. **Event Emitter Example**
```javascript
const EventEmitter = require('events');

class MyEmitter extends EventEmitter {}

const myEmitter = new MyEmitter();

myEmitter.on('event', () => {
    console.log('An event occurred!');
});

myEmitter.emit('event');
```

---

### 8. **Read and Write JSON in Node.js**
```javascript
const fs = require('fs');

const data = {
    name: "Sandeep Nath",
    skills: ["Node.js", "TypeScript", "AWS"],
};

// Write JSON to file
fs.writeFileSync('data.json', JSON.stringify(data, null, 2));

// Read JSON from file
const fileContent = fs.readFileSync('data.json', 'utf-8');
const parsedData = JSON.parse(fileContent);
console.log(parsedData);
```

---

### 9. **Real-Time Chat with WebSocket**
```javascript
const WebSocket = require('ws');

const wss = new WebSocket.Server({ port: 8080 });

wss.on('connection', ws => {
    ws.on('message', message => {
        console.log(`Received: ${message}`);
        ws.send(`Echo: ${message}`);
    });

    ws.send('Welcome to WebSocket server!');
});
```

---

### 10. **Node.js with MongoDB (CRUD Example)**
```javascript
const { MongoClient } = require('mongodb');

const url = 'mongodb://localhost:27017';
const client = new MongoClient(url);
const dbName = 'testDB';

async function run() {
    try {
        await client.connect();
        console.log('Connected to MongoDB');

        const db = client.db(dbName);
        const collection = db.collection('documents');

        // Create
        await collection.insertOne({ name: 'Document 1', value: 100 });

        // Read
        const docs = await collection.find().toArray();
        console.log('Documents:', docs);

        // Update
        await collection.updateOne({ name: 'Document 1' }, { $set: { value: 200 } });

        // Delete
        await collection.deleteOne({ name: 'Document 1' });
        console.log('Document deleted');
    } finally {
        await client.close();
    }
}

run().catch(console.dir);
```

Here are more advanced JavaScript and Node.js examples that showcase different concepts and patterns.

---

### 11. **File Upload with Multer in Express**
```javascript
const express = require('express');
const multer = require('multer');
const path = require('path');
const app = express();

// Set up storage engine for file uploads
const storage = multer.diskStorage({
    destination: (req, file, cb) => {
        cb(null, './uploads');
    },
    filename: (req, file, cb) => {
        cb(null, file.fieldname + '-' + Date.now() + path.extname(file.originalname));
    }
});

const upload = multer({ storage: storage });

// POST route to handle file upload
app.post('/upload', upload.single('file'), (req, res) => {
    res.send('File uploaded successfully!');
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 12. **MongoDB Aggregation Pipeline**
```javascript
const { MongoClient } = require('mongodb');

const url = 'mongodb://localhost:27017';
const client = new MongoClient(url);
const dbName = 'testDB';

async function run() {
    try {
        await client.connect();
        console.log('Connected to MongoDB');

        const db = client.db(dbName);
        const collection = db.collection('orders');

        // Example aggregation pipeline
        const results = await collection.aggregate([
            { $match: { status: 'shipped' } },
            { $group: { _id: '$customerId', totalSpent: { $sum: '$amount' } } },
            { $sort: { totalSpent: -1 } }
        ]).toArray();

        console.log('Aggregated Results:', results);
    } finally {
        await client.close();
    }
}

run().catch(console.dir);
```

---

### 13. **Debounce Function Example**
A debounce function is useful for limiting the rate at which a function is invoked.
```javascript
function debounce(func, delay) {
    let timeout;
    return function (...args) {
        clearTimeout(timeout);
        timeout = setTimeout(() => func(...args), delay);
    };
}

// Example usage
const handleSearch = debounce(function (event) {
    console.log('Searching for:', event.target.value);
}, 500);

document.getElementById('searchInput').addEventListener('input', handleSearch);
```

---

### 14. **Node.js Worker Threads for Parallel Processing**
Worker threads allow you to perform multi-threaded operations in Node.js.
```javascript
const { Worker, isMainThread, parentPort } = require('worker_threads');

if (isMainThread) {
    const worker = new Worker(__filename); // Launch worker

    worker.on('message', (message) => {
        console.log('Received from worker:', message);
    });

    worker.postMessage('Hello, worker!');
} else {
    parentPort.on('message', (message) => {
        console.log('Received from main thread:', message);
        parentPort.postMessage('Worker says hi!');
    });
}
```

---

### 15. **Using Redis for Caching in Node.js**
```javascript
const redis = require('redis');
const client = redis.createClient();

client.on('error', (err) => {
    console.log('Redis error:', err);
});

// Set a key-value pair
client.set('name', 'Sandeep', (err, reply) => {
    if (err) {
        console.log('Error setting value:', err);
    } else {
        console.log('Set value:', reply);
    }
});

// Get the value
client.get('name', (err, reply) => {
    if (err) {
        console.log('Error getting value:', err);
    } else {
        console.log('Retrieved value:', reply); // "Sandeep"
    }
});
```

---

### 16. **Rate Limiting with Express**
A simple rate limiter using an in-memory store.
```javascript
const express = require('express');
const app = express();

const RATE_LIMIT = 5; // Allow 5 requests per minute
const requestCounts = {};

app.use((req, res, next) => {
    const ip = req.ip;
    const currentTime = Date.now();
    const timeWindow = 60000; // 1 minute

    if (!requestCounts[ip]) {
        requestCounts[ip] = [];
    }

    // Remove outdated timestamps
    requestCounts[ip] = requestCounts[ip].filter(timestamp => currentTime - timestamp < timeWindow);

    if (requestCounts[ip].length >= RATE_LIMIT) {
        return res.status(429).send('Too many requests. Please try again later.');
    }

    // Log the current timestamp
    requestCounts[ip].push(currentTime);
    next();
});

app.get('/', (req, res) => {
    res.send('Hello World');
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 17. **Send Email Using Nodemailer in Node.js**
```javascript
const nodemailer = require('nodemailer');

const transporter = nodemailer.createTransport({
    service: 'gmail',
    auth: {
        user: 'your-email@gmail.com',
        pass: 'your-email-password'
    }
});

const mailOptions = {
    from: 'your-email@gmail.com',
    to: 'recipient-email@example.com',
    subject: 'Test Email from Node.js',
    text: 'This is a test email sent from Node.js using Nodemailer!'
};

transporter.sendMail(mailOptions, (error, info) => {
    if (error) {
        console.log('Error sending email:', error);
    } else {
        console.log('Email sent:', info.response);
    }
});
```

---

### 18. **Task Scheduler using `node-cron`**
Use `node-cron` to run tasks at specified intervals.
```javascript
const cron = require('node-cron');

// Run task every minute
cron.schedule('* * * * *', () => {
    console.log('Task running every minute');
});

// Run task every day at midnight
cron.schedule('0 0 * * *', () => {
    console.log('Task running at midnight');
});
```

---

### 19. **GraphQL Server with Apollo Server**
```javascript
const { ApolloServer, gql } = require('apollo-server');

// GraphQL schema
const typeDefs = gql`
    type Query {
        hello: String
    }
`;

// Resolver functions
const resolvers = {
    Query: {
        hello: () => 'Hello, world!',
    },
};

// Apollo Server setup
const server = new ApolloServer({ typeDefs, resolvers });

server.listen().then(({ url }) => {
    console.log(`Server ready at ${url}`);
});
```

---

### 20. **Custom Middleware in Express**
```javascript
const express = require('express');
const app = express();

// Custom middleware to log request details
app.use((req, res, next) => {
    console.log(`Method: ${req.method}, URL: ${req.url}`);
    next(); // Pass to the next middleware or route handler
});

app.get('/', (req, res) => {
    res.send('Hello, Express!');
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

Here are additional advanced JavaScript and Node.js examples that cover various use cases and concepts:

---

### 21. **Building a Simple Chat Server with Socket.io**
A real-time chat server using Socket.io in Node.js.
```javascript
const express = require('express');
const http = require('http');
const socketIo = require('socket.io');

const app = express();
const server = http.createServer(app);
const io = socketIo(server);

io.on('connection', (socket) => {
    console.log('A user connected');
    
    socket.on('disconnect', () => {
        console.log('A user disconnected');
    });

    socket.on('chat message', (msg) => {
        io.emit('chat message', msg);
    });
});

app.get('/', (req, res) => {
    res.sendFile(__dirname + '/index.html');
});

server.listen(3000, () => {
    console.log('Chat server running on http://localhost:3000');
});
```

---

### 22. **Using Sequelize ORM with MySQL**
Performing CRUD operations with Sequelize, a Node.js ORM for SQL databases.
```javascript
const { Sequelize, DataTypes } = require('sequelize');

// Connect to MySQL database
const sequelize = new Sequelize('mysql://root:password@localhost:3306/testdb');

// Define a User model
const User = sequelize.define('User', {
    name: {
        type: DataTypes.STRING,
        allowNull: false
    },
    email: {
        type: DataTypes.STRING,
        unique: true,
        allowNull: false
    }
});

async function run() {
    // Sync the database
    await sequelize.sync();

    // Create a new user
    const user = await User.create({ name: 'John Doe', email: 'john@example.com' });

    // Retrieve all users
    const users = await User.findAll();
    console.log('All users:', users);

    // Update a user
    await user.update({ name: 'John Smith' });

    // Delete a user
    await user.destroy();
}

run().catch(console.error);
```

---

### 23. **JWT Authentication with Refresh Token**
Implementing JWT authentication with access and refresh tokens for session management.
```javascript
const jwt = require('jsonwebtoken');
const express = require('express');
const app = express();
app.use(express.json());

const secretKey = 'mysecretkey';
const refreshTokens = []; // In-memory store (in production, use a database)

// Generate Access and Refresh Tokens
function generateTokens(user) {
    const accessToken = jwt.sign(user, secretKey, { expiresIn: '15m' });
    const refreshToken = jwt.sign(user, secretKey, { expiresIn: '7d' });
    return { accessToken, refreshToken };
}

// Token Refresh Endpoint
app.post('/token', (req, res) => {
    const refreshToken = req.body.token;
    if (!refreshToken || !refreshTokens.includes(refreshToken)) {
        return res.sendStatus(403);
    }

    jwt.verify(refreshToken, secretKey, (err, user) => {
        if (err) {
            return res.sendStatus(403);
        }
        const newTokens = generateTokens(user);
        res.json(newTokens);
    });
});

// Login Endpoint
app.post('/login', (req, res) => {
    const user = { username: req.body.username }; // Simplified for demo
    const { accessToken, refreshToken } = generateTokens(user);
    refreshTokens.push(refreshToken);
    res.json({ accessToken, refreshToken });
});

// Protected Route
app.get('/protected', (req, res) => {
    const authHeader = req.headers['authorization'];
    const token = authHeader && authHeader.split(' ')[1];
    
    if (!token) {
        return res.sendStatus(401);
    }

    jwt.verify(token, secretKey, (err, user) => {
        if (err) {
            return res.sendStatus(403);
        }
        res.json({ message: 'Protected data', user });
    });
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 24. **Implementing Rate Limiting with Redis**
Using Redis to implement rate limiting in a Node.js app.
```javascript
const express = require('express');
const redis = require('redis');
const app = express();
const client = redis.createClient();
const rateLimitWindow = 60; // 60 seconds
const rateLimitMax = 5; // Max 5 requests

client.on('error', (err) => {
    console.log('Error:', err);
});

// Rate Limiting Middleware
app.use((req, res, next) => {
    const ip = req.ip;
    const currentTime = Math.floor(Date.now() / 1000); // Current Unix timestamp
    const key = `rate_limit:${ip}:${currentTime}`;

    client.incr(key, (err, reply) => {
        if (err) return res.status(500).send('Server Error');

        if (reply > rateLimitMax) {
            return res.status(429).send('Rate limit exceeded. Please try again later.');
        }
        client.expire(key, rateLimitWindow); // Set expiration for key
        next();
    });
});

app.get('/', (req, res) => {
    res.send('Welcome to the rate-limited API!');
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 25. **Sending SMS with Twilio API**
Send an SMS using Twilio API in Node.js.
```javascript
const twilio = require('twilio');

// Twilio credentials
const accountSid = 'your_account_sid';
const authToken = 'your_auth_token';
const client = twilio(accountSid, authToken);

client.messages.create({
    body: 'Hello from Node.js!',
    from: '+1234567890', // Your Twilio number
    to: '+0987654321' // Recipient's number
})
.then(message => console.log('Message SID:', message.sid))
.catch(error => console.error('Error:', error));
```

---

### 26. **Building a Simple Todo List API with Express and MongoDB**
```javascript
const express = require('express');
const mongoose = require('mongoose');
const app = express();
app.use(express.json());

// Connect to MongoDB
mongoose.connect('mongodb://localhost:27017/todolist', { useNewUrlParser: true, useUnifiedTopology: true });

// Define Todo schema and model
const Todo = mongoose.model('Todo', {
    task: String,
    completed: { type: Boolean, default: false }
});

// Routes
app.get('/todos', async (req, res) => {
    const todos = await Todo.find();
    res.json(todos);
});

app.post('/todos', async (req, res) => {
    const newTodo = new Todo({
        task: req.body.task,
    });
    await newTodo.save();
    res.status(201).json(newTodo);
});

app.put('/todos/:id', async (req, res) => {
    const todo = await Todo.findByIdAndUpdate(req.params.id, req.body, { new: true });
    res.json(todo);
});

app.delete('/todos/:id', async (req, res) => {
    await Todo.findByIdAndDelete(req.params.id);
    res.status(204).send();
});

app.listen(3000, () => {
    console.log('Todo app running on http://localhost:3000');
});
```

---

### 27. **Using Passport.js for Local Authentication**
Implementing local strategy authentication with Passport.js.
```javascript
const express = require('express');
const passport = require('passport');
const LocalStrategy = require('passport-local').Strategy;
const app = express();
app.use(express.urlencoded({ extended: true }));

// Simple in-memory user store
const users = [{ id: 1, username: 'sandeep', password: 'password123' }];

passport.use(new LocalStrategy((username, password, done) => {
    const user = users.find(u => u.username === username);
    if (!user || user.password !== password) {
        return done(null, false, { message: 'Invalid credentials' });
    }
    return done(null, user);
}));

passport.serializeUser((user, done) => done(null, user.id));
passport.deserializeUser((id, done) => done(null, users.find(u => u.id === id)));

app.use(passport.initialize());

// Login endpoint
app.post('/login', passport.authenticate('local', {
    successRedirect: '/dashboard',
    failureRedirect: '/login',
}));

app.get('/dashboard', (req, res) => {
    res.send('Welcome to the dashboard');
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 28. **Using the Node.js `vm` Module to Execute Code**
The `vm` module allows you to compile and execute JavaScript code within Node.js.
```javascript
const vm = require('vm');

const context = { x: 10, y: 20 };
const code = 'x + y';

const result = vm.runInNewContext(code, context);
console.log('Result:', result); // 30
```

---

### 29. **Request Validation with Joi**
Using Joi to validate request bodies in an Express app.
```javascript
const express = require('express');
const Joi = require('joi');
const app = express();
app.use(express.json());

// Joi schema for validating input
const schema = Joi.object({
    username: Joi.string().min(3).required(),
    email: Joi.string().email().required()
});

app.post('/user', (req, res) => {
    const { error } = schema.validate(req.body);
    if (error) {
        return res.status(400).send(error.details[0].message);
    }
    res.send('User data is valid');
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 30. **File Compression with `zlib`**
Compressing files using Node.js `zlib` module.
```javascript
const fs = require('fs');
const zlib = require('zlib');

// Compress file
const gzip = zlib.createGzip();
const input = fs.createReadStream('input.txt');
const output = fs.createWriteStream('input.txt.gz');

input.pipe(gzip).pipe(output);

// Decompress file
const gunzip = zlib.createGunzip();
const inputGzip = fs.createReadStream('input.txt.gz');
const outputTxt = fs.createWriteStream('output.txt');

inputGzip.pipe(gunzip).pipe(outputTxt);
```

---
Here are additional advanced JavaScript and Node.js examples to continue enhancing your skills in various domains:

---

### 31. **Sending Push Notifications Using Firebase Cloud Messaging (FCM)**
Using Firebase Cloud Messaging (FCM) to send push notifications.
```javascript
const admin = require('firebase-admin');
const serviceAccount = require('./serviceAccountKey.json');

admin.initializeApp({
    credential: admin.credential.cert(serviceAccount)
});

const registrationToken = 'recipient_fcm_token';

const message = {
    notification: {
        title: 'Hello!',
        body: 'This is a push notification from Firebase.'
    },
    token: registrationToken
};

admin.messaging().send(message)
    .then((response) => {
        console.log('Successfully sent message:', response);
    })
    .catch((error) => {
        console.log('Error sending message:', error);
    });
```

---

### 32. **Implementing Web Scraping with `cheerio`**
A simple web scraping example using `cheerio` and `axios` to extract data from a webpage.
```javascript
const axios = require('axios');
const cheerio = require('cheerio');

async function scrapeData() {
    const { data } = await axios.get('https://example.com');
    const $ = cheerio.load(data);
    
    const titles = [];
    $('h1').each((index, element) => {
        titles.push($(element).text());
    });

    console.log('Extracted Titles:', titles);
}

scrapeData();
```

---

### 33. **Redis Caching for Database Results**
Using Redis to cache database results to improve performance.
```javascript
const redis = require('redis');
const mongoose = require('mongoose');
const client = redis.createClient();

mongoose.connect('mongodb://localhost:27017/testdb', { useNewUrlParser: true, useUnifiedTopology: true });

const Product = mongoose.model('Product', {
    name: String,
    price: Number
});

async function getProduct(productId) {
    const cacheKey = `product:${productId}`;

    // Check if data is available in Redis cache
    client.get(cacheKey, async (err, cachedData) => {
        if (cachedData) {
            console.log('Data from cache:', JSON.parse(cachedData));
        } else {
            const product = await Product.findById(productId);
            if (product) {
                client.setex(cacheKey, 3600, JSON.stringify(product)); // Cache data for 1 hour
                console.log('Data from database:', product);
            } else {
                console.log('Product not found');
            }
        }
    });
}

getProduct('60d4e6a7a0d90c001c45e5f3');
```

---

### 34. **Using `cluster` for Multi-Core Node.js Applications**
Using Node.js `cluster` module to utilize multiple CPU cores for scaling your application.
```javascript
const cluster = require('cluster');
const http = require('http');
const os = require('os');

if (cluster.isMaster) {
    const numCPUs = os.cpus().length;

    // Fork workers
    for (let i = 0; i < numCPUs; i++) {
        cluster.fork();
    }

    cluster.on('exit', (worker, code, signal) => {
        console.log(`Worker ${worker.process.pid} died`);
    });
} else {
    http.createServer((req, res) => {
        res.writeHead(200);
        res.end('Hello, Node.js Cluster!');
    }).listen(8000);
}
```

---

### 35. **Handling File Upload with Amazon S3**
Using AWS SDK to upload files to Amazon S3.
```javascript
const AWS = require('aws-sdk');
const fs = require('fs');

const s3 = new AWS.S3({
    accessKeyId: 'your-access-key-id',
    secretAccessKey: 'your-secret-access-key',
    region: 'us-east-1'
});

const uploadFile = (filePath) => {
    const fileContent = fs.readFileSync(filePath);

    const params = {
        Bucket: 'your-bucket-name',
        Key: 'your-file-key',
        Body: fileContent
    };

    s3.upload(params, (err, data) => {
        if (err) {
            console.error('Error uploading file:', err);
        } else {
            console.log('File uploaded successfully:', data.Location);
        }
    });
};

uploadFile('./local-file.txt');
```

---

### 36. **Using `express-session` for Session Management**
Implementing session management in an Express app using `express-session`.
```javascript
const express = require('express');
const session = require('express-session');
const app = express();

app.use(session({
    secret: 'your-secret-key',
    resave: false,
    saveUninitialized: true,
    cookie: { secure: false }  // Set secure to true if using HTTPS
}));

app.get('/', (req, res) => {
    if (req.session.views) {
        req.session.views++;
        res.send(`<h1>You've visited this page ${req.session.views} times</h1>`);
    } else {
        req.session.views = 1;
        res.send('<h1>Welcome to the session demo. Refresh to count visits.</h1>');
    }
});

app.listen(3000, () => {
    console.log('Session app running on http://localhost:3000');
});
```

---

### 37. **API Documentation with Swagger**
Generating API documentation with Swagger in an Express application.
```javascript
const express = require('express');
const swaggerJsDoc = require('swagger-jsdoc');
const swaggerUi = require('swagger-ui-express');
const app = express();

// Swagger configuration
const swaggerOptions = {
    swaggerDefinition: {
        info: {
            title: 'API Documentation',
            description: 'Test API documentation',
            version: '1.0.0'
        }
    },
    apis: ['./routes/*.js']
};

const swaggerDocs = swaggerJsDoc(swaggerOptions);

app.use('/api-docs', swaggerUi.serve, swaggerUi.setup(swaggerDocs));

app.listen(3000, () => {
    console.log('Swagger UI running on http://localhost:3000/api-docs');
});
```

---

### 38. **Handling Concurrent Requests with `async`/`await`**
Handling multiple asynchronous operations using `async`/`await`.
```javascript
const axios = require('axios');

async function fetchData() {
    try {
        const [response1, response2] = await Promise.all([
            axios.get('https://jsonplaceholder.typicode.com/posts/1'),
            axios.get('https://jsonplaceholder.typicode.com/posts/2')
        ]);

        console.log('Data from first request:', response1.data);
        console.log('Data from second request:', response2.data);
    } catch (error) {
        console.error('Error fetching data:', error);
    }
}

fetchData();
```

---

### 39. **Implementing WebSockets with `ws`**
Setting up a WebSocket server using the `ws` library in Node.js.
```javascript
const WebSocket = require('ws');
const wss = new WebSocket.Server({ port: 8080 });

wss.on('connection', (ws) => {
    console.log('A new client connected');
    
    ws.on('message', (message) => {
        console.log('Received:', message);
    });

    ws.send('Hello from WebSocket server!');
});

console.log('WebSocket server running on ws://localhost:8080');
```

---

### 40. **Using `async_hooks` to Track Asynchronous Events**
Tracking asynchronous operations using Node.js `async_hooks`.
```javascript
const async_hooks = require('async_hooks');
const fs = require('fs');

const hook = async_hooks.createHook({
    init(asyncId, type, triggerAsyncId, resource) {
        fs.writeSync(1, `Async operation ${type} with ID ${asyncId}\n`);
    },
    before(asyncId) {
        fs.writeSync(1, `Before async operation with ID ${asyncId}\n`);
    },
    after(asyncId) {
        fs.writeSync(1, `After async operation with ID ${asyncId}\n`);
    },
    destroy(asyncId) {
        fs.writeSync(1, `Async operation with ID ${asyncId} destroyed\n`);
    }
});

hook.enable();

// Example async operation to trigger hooks
setTimeout(() => {
    console.log('Async operation finished');
}, 1000);
```

---

### 41. **Proxy Server with `http-proxy-middleware`**
Creating a simple proxy server using `http-proxy-middleware` in an Express app.
```javascript
const express = require('express');
const { createProxyMiddleware } = require('http-proxy-middleware');
const app = express();

app.use('/api', createProxyMiddleware({ target: 'http://example.com', changeOrigin: true }));

app.listen(3000, () => {
    console.log('Proxy server running on http://localhost:3000');
});
```

---

### 42. **Sending Emails with SendGrid**
Sending emails using SendGrid's API in Node.js.
```javascript
const sgMail = require('@sendgrid/mail');
sgMail.setApiKey('your-sendgrid-api-key');

const msg = {
    to: 'recipient@example.com',
    from: 'sender@example.com',
    subject: 'Hello from Node.js',
    text: 'This is a test email sent using SendGrid.',
    html: '<strong>This is a test email sent using SendGrid.</strong>',
};

sgMail.send(msg)
    .then(() => {
        console.log('Email sent');
    })
    .catch((error) => {
        console.error(error);
    });
```

---
Here are more advanced JavaScript and Node.js examples to help you dive deeper into various concepts and applications:

---

### 43. **Using `sharp` for Image Processing**
`sharp` is a high-performance image processing library for Node.js, allowing you to resize, convert, and manipulate images.
```javascript
const sharp = require('sharp');

sharp('input-image.jpg')
    .resize(300, 200)
    .toFile('output-image.jpg', (err, info) => {
        if (err) {
            console.error('Error processing image:', err);
        } else {
            console.log('Image processed successfully:', info);
        }
    });
```

---

### 44. **Event-Driven Architecture with `EventEmitter`**
Using the `EventEmitter` class to create custom events and listeners in Node.js.
```javascript
const EventEmitter = require('events');
const eventEmitter = new EventEmitter();

// Event listener for 'order' event
eventEmitter.on('order', (orderId) => {
    console.log(`Order received: ${orderId}`);
});

// Triggering the 'order' event
eventEmitter.emit('order', '12345');
```

---

### 45. **Creating a Simple HTTP Server**
Setting up a simple HTTP server using Node.js's built-in `http` module.
```javascript
const http = require('http');

const server = http.createServer((req, res) => {
    res.statusCode = 200;
    res.setHeader('Content-Type', 'text/plain');
    res.end('Hello, World!\n');
});

server.listen(3000, () => {
    console.log('Server running at http://localhost:3000');
});
```

---

### 46. **Job Queue with `bull` (Redis-based)**
`bull` is a library for handling jobs and queues, using Redis as a backend.
```javascript
const Queue = require('bull');

// Create a new queue
const emailQueue = new Queue('emailQueue', 'redis://127.0.0.1:6379');

// Define a job processor
emailQueue.process(async (job) => {
    console.log('Sending email to:', job.data.email);
    // Simulate email sending process
    return new Promise((resolve) => setTimeout(resolve, 1000));
});

// Add a job to the queue
emailQueue.add({ email: 'user@example.com' });

// Handling job completion
emailQueue.on('completed', (job, result) => {
    console.log(`Job ${job.id} completed`);
});
```

---

### 47. **Caching HTTP Responses with `node-cache`**
Using `node-cache` to cache HTTP responses in memory for fast access.
```javascript
const express = require('express');
const NodeCache = require('node-cache');
const app = express();
const cache = new NodeCache();

// Mock function to fetch data from a database
function fetchData() {
    return { name: 'John Doe', age: 30 };
}

// Route that uses caching
app.get('/user', (req, res) => {
    const cacheKey = 'user';

    // Check if data is in cache
    const cachedData = cache.get(cacheKey);
    if (cachedData) {
        return res.json(cachedData);
    }

    // If not cached, fetch data and store it in cache
    const data = fetchData();
    cache.set(cacheKey, data, 60); // Cache for 60 seconds
    res.json(data);
});

app.listen(3000, () => {
    console.log('Server running at http://localhost:3000');
});
```

---

### 48. **Web Scraping with Puppeteer (Headless Browser)**
Using Puppeteer to scrape content from web pages by simulating a headless browser.
```javascript
const puppeteer = require('puppeteer');

async function scrapeWebsite() {
    const browser = await puppeteer.launch();
    const page = await browser.newPage();
    
    await page.goto('https://example.com');
    const title = await page.title();
    
    console.log('Page Title:', title);
    
    await browser.close();
}

scrapeWebsite();
```

---

### 49. **Creating a REST API with Express and MongoDB**
Building a REST API using Express and MongoDB with basic CRUD operations.
```javascript
const express = require('express');
const mongoose = require('mongoose');
const app = express();
app.use(express.json());

// Connect to MongoDB
mongoose.connect('mongodb://localhost:27017/api', { useNewUrlParser: true, useUnifiedTopology: true });

// Define a simple model
const Post = mongoose.model('Post', {
    title: String,
    content: String
});

// CRUD Endpoints

// Create a new post
app.post('/posts', async (req, res) => {
    const post = new Post(req.body);
    await post.save();
    res.status(201).json(post);
});

// Get all posts
app.get('/posts', async (req, res) => {
    const posts = await Post.find();
    res.json(posts);
});

// Get a single post by ID
app.get('/posts/:id', async (req, res) => {
    const post = await Post.findById(req.params.id);
    if (!post) return res.status(404).send('Post not found');
    res.json(post);
});

// Update a post
app.put('/posts/:id', async (req, res) => {
    const post = await Post.findByIdAndUpdate(req.params.id, req.body, { new: true });
    if (!post) return res.status(404).send('Post not found');
    res.json(post);
});

// Delete a post
app.delete('/posts/:id', async (req, res) => {
    const post = await Post.findByIdAndDelete(req.params.id);
    if (!post) return res.status(404).send('Post not found');
    res.status(204).send();
});

app.listen(3000, () => {
    console.log('API server running at http://localhost:3000');
});
```

---

### 50. **Implementing OAuth 2.0 Authentication**
Using OAuth 2.0 for third-party authentication (e.g., Google).
```javascript
const express = require('express');
const passport = require('passport');
const GoogleStrategy = require('passport-google-oauth20').Strategy;

const app = express();

// Configure Passport.js with Google OAuth strategy
passport.use(new GoogleStrategy({
    clientID: 'your-google-client-id',
    clientSecret: 'your-google-client-secret',
    callbackURL: 'http://localhost:3000/auth/google/callback'
}, (accessToken, refreshToken, profile, done) => {
    return done(null, profile);
}));

// Serialize user info
passport.serializeUser((user, done) => done(null, user));
passport.deserializeUser((obj, done) => done(null, obj));

// Express routes
app.get('/auth/google',
    passport.authenticate('google', { scope: ['profile', 'email'] })
);

app.get('/auth/google/callback',
    passport.authenticate('google', { failureRedirect: '/' }),
    (req, res) => {
        res.send('You are logged in');
    }
);

app.listen(3000, () => {
    console.log('Server running at http://localhost:3000');
});
```

---

### 51. **Running Asynchronous Tasks in Parallel with `Promise.all`**
Running multiple asynchronous tasks in parallel using `Promise.all`.
```javascript
const axios = require('axios');

async function fetchMultipleUrls() {
    const urls = [
        'https://jsonplaceholder.typicode.com/posts/1',
        'https://jsonplaceholder.typicode.com/posts/2',
        'https://jsonplaceholder.typicode.com/posts/3'
    ];

    const responses = await Promise.all(urls.map(url => axios.get(url)));

    responses.forEach(response => {
        console.log(response.data);
    });
}

fetchMultipleUrls();
```

---

### 52. **Database Transactions with Sequelize**
Performing a transaction using Sequelize ORM to ensure atomicity of operations.
```javascript
const { Sequelize, DataTypes, Op } = require('sequelize');
const sequelize = new Sequelize('mysql://root:password@localhost:3306/testdb');

// Define User model
const User = sequelize.define('User', {
    name: DataTypes.STRING,
    balance: DataTypes.INTEGER
});

async function transferFunds(senderId, receiverId, amount) {
    const transaction = await sequelize.transaction();

    try {
        const sender = await User.findByPk(senderId, { transaction });
        const receiver = await User.findByPk(receiverId, { transaction });

        if (sender.balance < amount) {
            throw new Error('Insufficient funds');
        }

        sender.balance -= amount;
        receiver.balance += amount;

        await sender.save({ transaction });
        await receiver.save({ transaction });

        await transaction.commit();
        console.log('Transaction successful');
    } catch (error) {
        await transaction.rollback();
        console.error('Transaction failed:', error);
    }
}

sequelize.sync().then(() => {
    transferFunds(1, 2, 50);
});
```

---

### 53. **Using `pm2` for Process Management**
Running and managing Node.js applications with `pm2`, a process manager.
```bash
# Install pm2 globally
npm install pm2 -g

# Start your application with pm2
pm2 start app.js

# View application status
pm2 status

# Restart application
pm2 restart app.js

# View logs
pm2 logs

# Monitor resource usage
pm2 monit
```

---

### 54. **Cross-Origin Resource Sharing (CORS) in Express**
Enabling CORS in an Express application to allow requests from other domains.
```javascript
const express = require('express');
const cors = require('cors');
const app = express();

// Enable CORS for all origins
app.use(cors());

// Specific CORS configuration
app.use(cors({
    origin: 'http://example.com',
    methods: ['GET', 'POST'],
    allowedHeaders: ['Content-Type']
}));

app.get('/', (req, res) => {
    res.send('CORS-enabled app');
});

app.listen(3000, () => {


    console.log('CORS app running at http://localhost:3000');
});
```

---

### 55. **File Upload with `multer` in Express**
Handling file uploads with `multer` middleware in Express.
```javascript
const express = require('express');
const multer = require('multer');
const app = express();

// Set up multer storage
const storage = multer.diskStorage({
    destination: (req, file, cb) => {
        cb(null, 'uploads/');
    },
    filename: (req, file, cb) => {
        cb(null, Date.now() + '-' + file.originalname);
    }
});
const upload = multer({ storage: storage });

app.post('/upload', upload.single('file'), (req, res) => {
    res.send('File uploaded successfully');
});

app.listen(3000, () => {
    console.log('File upload server running at http://localhost:3000');
});
```

---

Here are more advanced JavaScript and Node.js examples to further expand your toolkit:

---

### 56. **Implementing JWT Authentication**
Using JSON Web Tokens (JWT) for authentication in an Express application.
```javascript
const express = require('express');
const jwt = require('jsonwebtoken');
const app = express();
const SECRET_KEY = 'your-secret-key';

app.use(express.json());

// Generate JWT Token
app.post('/login', (req, res) => {
    const { username, password } = req.body;
    
    // Assume credentials are valid
    const user = { username };
    
    // Generate token
    const token = jwt.sign(user, SECRET_KEY, { expiresIn: '1h' });
    res.json({ token });
});

// Protected Route
app.get('/protected', (req, res) => {
    const token = req.headers['authorization'];

    if (!token) return res.status(403).send('Token required');

    jwt.verify(token, SECRET_KEY, (err, decoded) => {
        if (err) return res.status(403).send('Invalid token');
        res.json({ message: 'This is protected data', user: decoded });
    });
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 57. **Error Handling Middleware in Express**
Implementing custom error handling middleware for improved error management in Express.
```javascript
const express = require('express');
const app = express();

app.use(express.json());

// Sample route
app.get('/', (req, res) => {
    throw new Error('Something went wrong!');
});

// Custom error handling middleware
app.use((err, req, res, next) => {
    console.error(err.message);
    res.status(500).json({ error: err.message });
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 58. **Using `dotenv` for Environment Variables**
Storing sensitive information in environment variables using `dotenv`.
```javascript
// .env file
// DB_URI=mongodb://localhost:27017/mydb
// SECRET_KEY=your-secret-key

const express = require('express');
const dotenv = require('dotenv');
dotenv.config();

const app = express();

// Accessing environment variables
const dbURI = process.env.DB_URI;
const secretKey = process.env.SECRET_KEY;

app.get('/', (req, res) => {
    res.json({ dbURI, secretKey });
});

app.listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 59. **File Streaming with `fs.createReadStream`**
Stream files efficiently from the filesystem with `fs.createReadStream`.
```javascript
const fs = require('fs');
const http = require('http');

http.createServer((req, res) => {
    const filePath = 'large-file.txt';
    const fileStream = fs.createReadStream(filePath);

    res.writeHead(200, { 'Content-Type': 'text/plain' });
    fileStream.pipe(res); // Stream file directly to the response

    fileStream.on('end', () => {
        console.log('File streaming completed');
    });

}).listen(3000, () => {
    console.log('Server running on http://localhost:3000');
});
```

---

### 60. **Async/Await with Error Handling**
Using `async/await` with proper error handling using `try/catch` blocks.
```javascript
const axios = require('axios');

async function fetchData() {
    try {
        const response = await axios.get('https://jsonplaceholder.typicode.com/posts/1');
        console.log('Data:', response.data);
    } catch (error) {
        console.error('Error fetching data:', error);
    }
}

fetchData();
```

---

### 61. **WebSocket with `socket.io`**
Setting up a WebSocket server with `socket.io` for real-time communication.
```javascript
const express = require('express');
const http = require('http');
const socketIo = require('socket.io');
const app = express();
const server = http.createServer(app);
const io = socketIo(server);

io.on('connection', (socket) => {
    console.log('A user connected');
    
    socket.on('disconnect', () => {
        console.log('A user disconnected');
    });

    // Listen for message from client
    socket.on('chat message', (msg) => {
        io.emit('chat message', msg); // Broadcast the message to all clients
    });
});

app.get('/', (req, res) => {
    res.send('<h1>WebSocket Server</h1>');
});

server.listen(3000, () => {
    console.log('WebSocket server running at http://localhost:3000');
});
```

---

### 62. **Building a Simple To-Do List with Express and MongoDB**
A simple CRUD to-do list application using Express and MongoDB.
```javascript
const express = require('express');
const mongoose = require('mongoose');
const app = express();
app.use(express.json());

// Connect to MongoDB
mongoose.connect('mongodb://localhost:27017/todolist', { useNewUrlParser: true, useUnifiedTopology: true });

// To-Do Schema and Model
const Todo = mongoose.model('Todo', {
    text: String,
    completed: { type: Boolean, default: false }
});

// Create a new to-do item
app.post('/todos', async (req, res) => {
    const todo = new Todo({
        text: req.body.text
    });
    await todo.save();
    res.status(201).json(todo);
});

// Get all to-do items
app.get('/todos', async (req, res) => {
    const todos = await Todo.find();
    res.json(todos);
});

// Update a to-do item
app.put('/todos/:id', async (req, res) => {
    const todo = await Todo.findByIdAndUpdate(req.params.id, req.body, { new: true });
    res.json(todo);
});

// Delete a to-do item
app.delete('/todos/:id', async (req, res) => {
    await Todo.findByIdAndDelete(req.params.id);
    res.status(204).send();
});

app.listen(3000, () => {
    console.log('To-Do List API running on http://localhost:3000');
});
```

---

### 63. **Creating an Express Rate Limiter with `express-rate-limit`**
Preventing brute-force attacks by limiting the number of requests with `express-rate-limit`.
```javascript
const express = require('express');
const rateLimit = require('express-rate-limit');
const app = express();

// Create a rate limiter
const limiter = rateLimit({
    windowMs: 15 * 60 * 1000, // 15 minutes
    max: 100, // limit each IP to 100 requests per windowMs
    message: 'Too many requests from this IP, please try again later.'
});

// Apply rate limiter to all routes
app.use(limiter);

app.get('/', (req, res) => {
    res.send('Welcome to the API');
});

app.listen(3000, () => {
    console.log('Rate-limited app running on http://localhost:3000');
});
```

---

### 64. **Multi-Part Form Data Upload with `formidable`**
Handling multi-part form data (like file uploads) using `formidable`.
```javascript
const express = require('express');
const formidable = require('formidable');
const app = express();

app.post('/upload', (req, res) => {
    const form = new formidable.IncomingForm();

    form.parse(req, (err, fields, files) => {
        if (err) {
            res.status(500).send('Error processing form data');
            return;
        }

        res.json({ fields, files });
    });
});

app.listen(3000, () => {
    console.log('Formidable upload server running on http://localhost:3000');
});
```

---

### 65. **Creating a Basic Authentication System**
Implementing basic authentication with middleware in Express.
```javascript
const express = require('express');
const app = express();

// Basic authentication middleware
const basicAuth = (req, res, next) => {
    const auth = req.headers.authorization;
    if (!auth || auth !== 'Basic YWRtaW46YWRtaW4=') {  // base64 for 'admin:admin'
        return res.status(401).send('Authentication required');
    }
    next();
};

// Use basic authentication middleware
app.use(basicAuth);

app.get('/', (req, res) => {
    res.send('You are authenticated');
});

app.listen(3000, () => {
    console.log('Basic authentication app running on http://localhost:3000');
});
```

---

### 66. **Using `uuid` for Unique Identifiers**
Generating unique IDs using `uuid` in Node.js.
```javascript
const { v4: uuidv4 } = require('uuid');

const uniqueID = uuidv4();
console.log('Generated Unique ID:', uniqueID);
```

---

### 67. **Creating a Background Worker Using `node-cron`**
Scheduling background tasks with `node-cron` to run periodically.
```javascript
const cron = require('node-cron');

// Run a task every minute
cron.schedule('* * * * *', () => {
    console.log('Task is running every minute');
});
```

---

### 68. **Building a Simple GraphQL API with Apollo Server**
Creating a simple GraphQL API with Apollo Server.
```javascript
const { ApolloServer, gql } = require('apollo-server');

// Define GraphQL schema
const typeDefs = gql`
  type Query {
    hello: String
  }
`;

// Define resolvers
const resolvers = {
  Query: {
   

 hello: () => 'Hello, World!'
  }
};

// Create Apollo Server
const server = new ApolloServer({ typeDefs, resolvers });

server.listen().then(({ url }) => {
  console.log(`Server ready at ${url}`);
});
```

---
