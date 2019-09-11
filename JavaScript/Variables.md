`var`, `let` and `const` keywords are used in JavaScript to declare variables.

```javascript
var a;
let b;
const c = 10;
```

Attempt to access an undeclared variable results in `ReferenceError`.

```javascript
console.log(a); // ReferenceError: a is not defined
```

## `var`, `let` and `const`

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

A variable declared using the `var` or `let` statement with no assigned value specified has the value of `undefined`.

```javascript
var a;
let b;
console.log(a); // undefined
console.log(b); // undefined
```

Variables declared using `let` and `const` are block scoped.

```javascript
{
  let a = 10;
}
console.log(a); // ReferenceError: a is not defined
```
