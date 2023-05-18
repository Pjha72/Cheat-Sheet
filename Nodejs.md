# Node.js Cheatsheet

## Basics

- **Create a new Node.js project**: `npm init`
- **Install dependencies**: `npm install <package>`
- **Run a Node.js script**: `node <filename.js>`
- **Execute a Node.js file with Nodemon**: `nodemon <filename.js>`

## Modules and Packages

- **Import a module**: `const moduleName = require('module')`
- **Export a module**: `module.exports = { ... }`
- **Use a built-in module**: `const fs = require('fs')`
- **Install a package globally**: `npm install -g <package>`
- **Install a package locally**: `npm install <package>`

## File System

- **Read a file**: `fs.readFile('<filename>', 'utf8', (err, data) => { ... })`
- **Write to a file**: `fs.writeFile('<filename>', 'data', (err) => { ... })`
- **Check if a file exists**: `fs.existsSync('<filename>')`

## HTTP

- **Create an HTTP server**: 

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!');
});

server.listen(3000, 'localhost', () => {
  console.log('Server is running on port 3000');
});```
