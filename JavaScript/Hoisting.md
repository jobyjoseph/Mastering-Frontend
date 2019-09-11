In JavaScript, we can refer to a variable declared later. This is called hoisting.

```javascript
console.log(a); // undefined
var a;
```

Hoisted variables return a value of `undefined`.

```javascript
console.log(a); // undefined, not 6
var a = 6;
```

Variable is hoisted, either to the top of function or to the top of file.

```javascript
console.log(a); // ReferenceError: a is not defined
function b() {
  var a = 10; // This 'a' is hoisted to the top of b, not beyond.
}
```

Variables declared using `let` or `const` are not hoisted.

```javascript
console.log(a); // ReferenceError: Cannot access 'a' before initialization
let a; 
```
