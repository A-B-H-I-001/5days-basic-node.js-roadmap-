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
Day 3: Express.js Introduction
Topics Covered:
Introduction to Express.js
Creating a basic Express server
Handling routes (GET, POST, PUT, DELETE)
Using Middleware in Express
Example Code:
js
Copy code
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send("Welcome to Home Page");
});

app.listen(3000, () => {
  console.log("Server is running at http://localhost:3000");
});
Day 4: MongoDB Basics
Topics Covered:
Introduction to MongoDB
Setting up a MongoDB database
Using Mongoose to interact with MongoDB
Basic CRUD operations in MongoDB
Example Code:
js
Copy code
const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost:27017/myDB', { useNewUrlParser: true, useUnifiedTopology: true })
  .then(() => console.log('Connected to MongoDB'))
  .catch(err => console.log('Connection Error:', err));
Day 5: REST API with Express & MongoDB
Topics Covered:
Creating a simple REST API with Express.js and MongoDB
Performing CRUD operations (Create, Read, Update, Delete)
Setting up routes for the API
Example Code:
js
Copy code
const express = require('express');
const mongoose = require('mongoose');
const app = express();
app.use(express.json());

// MongoDB connection
mongoose.connect('mongodb://localhost:27017/userDB', { useNewUrlParser: true, useUnifiedTopology: true });

// User Schema
const userSchema = new mongoose.Schema({
  name: String,
  email: String
});
const User = mongoose.model('User', userSchema);

// API Routes
app.post('/users', async (req, res) => {
  const user = new User(req.body);
  await user.save();
  res.send('User added');
});

app.get('/users', async (req, res) => {
  const users = await User.find();
  res.send(users);
});

app.listen(3000, () => {
  console.log("Server is running on http://localhost:3000");
});
Day 6: Project Completion & Deployment
Topics Covered:
Completing the User Management API
Deploying the app to Heroku
Steps for Deployment:
Heroku account create karo.
Heroku CLI install karo aur login karo:
bash
Copy code
heroku login
Apne code ko Git ke through Heroku pe push karo:
bash
Copy code
git init
git add .
git commit -m "Initial commit"
git remote add origin <heroku-repository-url>
git push heroku main
App ko Heroku pe open karo:
bash
Copy code
heroku open
Conclusion
By following this roadmap, you will gain hands-on experience in Node.js, Express.js, and MongoDB. By the end of Day 6, you'll have a User Management API and know how to deploy it to Heroku.

Good luck with your learning journey! 🚀

Project Folder Structure:
lua
Copy code
/my-node-app
    |-- /node_modules
    |-- /models
    |-- /routes
    |-- /controllers
    |-- app.js
    |-- package.json
    |-- README.md
