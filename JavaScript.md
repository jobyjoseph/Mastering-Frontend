# JavaScript

### Asynchronous JavaScript
General asynchronous programming concepts - https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Concepts

> When a web app runs in a browser and it executes an intensive chunk of code without returning control to the browser, the browser can appear to be frozen. This is called **blocking**.

> JavaScript is **single threaded**.

> Web workers allow you to send some of the JavaScript processing off to a separate thread, called a worker, so that you can run multiple JavaScript chunks simultaneously.

> Web workers are pretty useful, but they do have their limitations. A major one is they are not able to access the DOM — you can't get a worker to directly do anything to update the UI.

HTML5 Web Workers for AJAX Requests - http://techslides.com/html5-web-workers-for-ajax-requests

> Web worker script can execute AJAX request.

### Memory Management
Memory Management - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management

> Reference-counting garbage collection: An object is said to be "garbage", or collectible if there are zero references pointing to it. There is a limitation when it comes to circular references.

> Mark-and-sweep algorithm: Starting from the roots, the garbage collector will thus find all reachable objects and collect all non-reachable objects. As of 2012, all modern browsers ship a mark-and-sweep garbage-collector.

> In Node.js, The max amount of available heap memory can be increased with a flag `--max-old-space-size`.

> In Node.js, We can expose the garbage collector for debugging memory issues using a flag `--expose-gc --inspect` and the Chrome Debugger.

### Event Loop
Concurrency model and Event Loop - https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop

> A web worker or a cross-origin `iframe` has its own stack, heap, and message queue. Two distinct runtimes can only communicate through sending messages via the `postMessage` method.
