# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js servers: hanging on long-running requests.  The `server.js` file shows a server that performs a 5-second delay, blocking the event loop and preventing other requests from being processed. The `serverSolution.js` file demonstrates the correct way to avoid this using asynchronous operations.

## How to Reproduce

1. Clone this repository.
2. Run `node server.js`.
3. Open multiple tabs and send requests to `http://localhost:3000`. Observe that after the first request, subsequent requests hang.

## Solution

The solution uses asynchronous operations (e.g., timers or workers) to prevent blocking the event loop.  This ensures that the server remains responsive even under heavy load.