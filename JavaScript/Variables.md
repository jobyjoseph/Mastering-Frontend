`var`, `let` and `const` keywords are used in JavaScript to declare variables.

```javascript
var a;
let b;
const c = 10;
```

## `var`

`var` is function scoped.

```javascript
function a(){
  var b = 10; // b is not accessible outside a
}
a();
console.log(b); // ReferenceError: b is not defined
```

A global variable can be created by declaring it outside all functions.

```javascript
var name = "Joby"
function a(){
  console.log(name);
}
a(); // "Joby"
console.log(name); // "Joby"
```
