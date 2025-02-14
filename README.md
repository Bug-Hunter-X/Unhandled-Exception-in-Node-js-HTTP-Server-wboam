# Node.js HTTP Server Bug

This repository demonstrates a common error when creating an HTTP server in Node.js: forgetting to provide a callback function to the `server.listen()` method.

## Bug Description

The `bug.js` file contains code that attempts to create an HTTP server. However, it omits the callback function in `server.listen()`, leading to an unhandled exception if there's an error during server startup.  This can make debugging difficult.

## Solution

The `bugSolution.js` file shows the corrected code.  By adding a callback function, you handle potential errors and receive confirmation when the server starts successfully.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js`.  Observe that the server doesn't start, and there's likely a cryptic error message (or no indication at all).
4. Run `node bugSolution.js`. Observe that the server starts and a confirmation message is printed to the console.

This example highlights the importance of error handling in asynchronous operations within Node.js.