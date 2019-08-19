# Mastering Frontend

## Asynchronous JavaScript

## Memory Management
Memory Management - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management

> Reference-counting garbage collection: An object is said to be "garbage", or collectible if there are zero references pointing to it. There is a limitation when it comes to circular references.

> Mark-and-sweep algorithm: Starting from the roots, the garbage collector will thus find all reachable objects and collect all non-reachable objects. As of 2012, all modern browsers ship a mark-and-sweep garbage-collector.

> In Node.js, The max amount of available heap memory can be increased with a flag `--max-old-space-size`.

> In Node.js, We can expose the garbage collector for debugging memory issues using a flag `--expose-gc --inspect` and the Chrome Debugger.

## Event Loop
Concurrency model and Event Loop - https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop

> A web worker or a cross-origin `iframe` has its own stack, heap, and message queue. Two distinct runtimes can only communicate through sending messages via the `postMessage` method.
