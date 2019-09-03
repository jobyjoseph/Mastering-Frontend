## Async Await

https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await

`async` and `await` are part of ES8

We put `async` infront of any function to turn it to an async function. `async` turns any function to a Promise.

```javascript
// Async function
async function hello(){
  return "hello"
}

// Resolving the promise
hello().then(function(data){
  console.log(data); // "hello"
})
```
