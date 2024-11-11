# 6-Day Node.js, Express, and MongoDB Learning Roadmap

Welcome to the **6-Day Node.js, Express, and MongoDB Roadmap**! This roadmap is designed for beginners to help you understand the basics of **Node.js**, **Express.js**, and **MongoDB**. By the end of this 6-day plan, you'll build a **User Management API** and deploy it to **Heroku**.

## Table of Contents
1. [Day 1: Node.js Basics](#day-1-nodejs-basics)
2. [Day 2: Asynchronous Programming in Node.js](#day-2-asynchronous-programming-in-nodejs)
3. [Day 3: Express.js Introduction](#day-3-expressjs-introduction)
4. [Day 4: MongoDB Basics](#day-4-mongodb-basics)
5. [Day 5: REST API with Express & MongoDB](#day-5-rest-api-with-express-mongodb)
6. [Day 6: Project Completion & Deployment](#day-6-project-completion-deployment)

---

## Day 1: Node.js Basics

### Topics Covered:
- **Node.js** introduction
- Installing Node.js
- Writing your first Node.js script
- Working with the **File System** module
- Introduction to **npm** (Node Package Manager)

### Example Code:

```js
console.log("Hello, Node.js!");

// File system example:
const fs = require('fs');
fs.writeFileSync('hello.txt', 'Hello from Node.js!');


Day 2: Asynchronous Programming in Node.js
Topics Covered:
Asynchronous Programming in Node.js
Callbacks, Promises, Async/Await
Using setTimeout and setInterval
Example Code:
js
Copy code
setTimeout(() => {
  console.log("This runs after 2 seconds");
}, 2000);
