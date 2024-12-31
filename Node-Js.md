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
