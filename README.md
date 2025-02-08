# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js applications: server unresponsiveness caused by a long-running synchronous operation blocking the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version.

## Problem
The original code attempts to perform a very intensive calculation within the request handler. This blocks the event loop, preventing the server from handling other requests and potentially causing it to hang or become unresponsive.

## Solution
The solution uses asynchronous operations (promises or async/await) to prevent blocking the event loop.  The long-running task is offloaded, allowing the server to remain responsive.

## How to Run
1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `node server.js` (buggy version) or `node serverSolution.js` (corrected version).
4. Observe the server's behavior and response times.