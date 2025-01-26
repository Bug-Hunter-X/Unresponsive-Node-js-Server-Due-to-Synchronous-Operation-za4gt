# Unresponsive Node.js Server Due to Synchronous Operation

This repository demonstrates a common issue in Node.js applications where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code.  The solution (`bugSolution.js`) illustrates how to address this using asynchronous operations.

## Problem

The server uses a `while` loop to simulate a long-running task, tying up the event loop for 5 seconds. During this time, the server is unable to handle any other requests, leading to unresponsiveness.

## Solution

The solution involves using asynchronous operations (e.g., `setTimeout` or promises) to prevent blocking the event loop.  This allows the server to continue handling other requests while the long-running task is executed in the background.