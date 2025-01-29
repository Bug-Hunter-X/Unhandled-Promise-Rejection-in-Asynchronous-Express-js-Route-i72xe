# Unhandled Promise Rejection in Asynchronous Express.js Route

This repository demonstrates a common error in Node.js applications: unhandled promise rejections in asynchronous callbacks.  The `bug.js` file showcases an Express.js route where an error within a `setTimeout` callback is not properly handled, leading to a server crash without clear indication of the cause.  The `bugSolution.js` file provides a corrected version, showcasing proper error handling using `try...catch` blocks or promise `.catch()` for better robustness and more informative error logging.

## How to Reproduce the Bug

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `node bug.js`.
4. Make a request to `http://localhost:3000`.  About half the time you should see the server crash without informative error details in the console.

## Solution

The solution lies in handling potential errors within the asynchronous callback.  Examine `bugSolution.js` for a corrected approach using `try...catch` for better error handling and logging.