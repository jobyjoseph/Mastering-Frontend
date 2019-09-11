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

Global variables are properties of the global object.

```javascript
var a = 7;
console.log(window.a); // 7
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

`let` or `const` variables cannot be redeclared.

```javascript
var a = 7;
let a = 8; // SyntaxError: Identifier 'a' has already been declared
console.log(a);
```

Constant variables are created using `const` keyword. Once initialized, the value cannot be changed.

```javascript
const a = 6;
a = 7; // TypeError: Assignment to constant variable.
console.log(a);
```

Variables declared using `const` should be initialized.

```javascript
const a;
a = 8; // SyntaxError: Missing initializer in const declaration
console.log(a);
```
