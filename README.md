# Node.js Server Unresponsiveness Due to Long-Running Task

This repository demonstrates a common issue in Node.js applications: server unresponsiveness due to long-running tasks in request handlers.  The `server.js` file contains a simple HTTP server that performs a computationally expensive task within the request handler. This blocks the event loop, preventing the server from responding to other requests.

The solution, `serverSolution.js`, demonstrates using asynchronous operations (specifically `setTimeout` in this case, though other methods like `Promises` and `async/await` are also applicable) to prevent the event loop from being blocked.