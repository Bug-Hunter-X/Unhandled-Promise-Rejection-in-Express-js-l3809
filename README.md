# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections.  When an asynchronous operation within a route handler throws an error, and that error isn't properly caught, it can lead to the application crashing silently or behaving unexpectedly.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides a solution using error handling.

## How to reproduce

1. Clone the repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js`. You'll notice the server starts, but the error isn't logged to the console, and the application may behave unexpectedly.
4. Run `node bugSolution.js`.  This version properly handles the error using a `catch` block.