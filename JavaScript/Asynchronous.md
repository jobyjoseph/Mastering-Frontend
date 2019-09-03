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

`await` can pause your code on that line until the promise fulfills, then return the resulting value.

`await` only works inside of `async` functions.

Error handling:

```javascript
async function wrongAPI(){
  try {
    // Trying to call an invalid API. Given url does not exist
    let response = await fetch("http://example.com/api");
    return response;
  } catch(e) {
    return e.message;
  }
}

wrongAPI().then(function(data){
  console.log(data); // Prints "Failed to fetch" which comes from e.message
});
```

We can handle errors either by using `try...catch` inside async function or using `.catch()` on the returned promise.
