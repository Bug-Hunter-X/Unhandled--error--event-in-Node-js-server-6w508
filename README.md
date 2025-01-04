# Unhandled 'error' event in Node.js
This repository demonstrates a common error in Node.js server development: unhandled errors.  The server crashes without providing informative error messages when facing unexpected problems.

## Problem
The provided `server.js` starts a simple HTTP server. However, it lacks proper error handling.  If the server encounters an error (e.g., network issue, invalid request), it crashes without logging the error, making debugging difficult.

## Solution
The `serverSolution.js` shows how to correctly handle the 'error' event using the `server.on('error', ...)` method.  This ensures that errors are logged to the console, preventing unexpected crashes and providing valuable debugging information.

## How to reproduce
1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `node server.js`.
4. Attempt to cause an error (e.g., by interrupting the network connection).
5. Observe the lack of informative error messages and the server crash.
6. Run `node serverSolution.js` and repeat step 4. Note that error messages are now logged to the console, providing helpful debugging information.