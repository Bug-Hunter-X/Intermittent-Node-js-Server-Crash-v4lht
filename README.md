# Intermittent Node.js Server Crash

This repository demonstrates a bug causing intermittent crashes in a simple Node.js HTTP server. The server appears to function normally for a period, then unexpectedly terminates without any error messages or logs.

## Bug Description

A Node.js server built using the `http` module crashes intermittently. The crash occurs without any apparent pattern or error messages in the console.  The server handles requests correctly before crashing.

## Solution

The solution involves identifying and handling potential uncaught exceptions.  While there's no explicit error in the original code, unhandled exceptions within the request listener,  or even in asynchronous operations triggered by the request, could lead to the crashes.

The provided solution includes a `try...catch` block in the request listener to improve error handling.