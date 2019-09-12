There are 7 primitive data types.

1. Boolean: `true` and `false` are the only values under Boolean type.

```javascript
let b1 = true;
let b2 = false;
```
2. null: `null` is a primitive type with only one valid value, ie `null`

```javascript
let a = null // null represents no value
```

3. undefined: `undefined` is a primitive type with only one valid value, ie `undefined`

```javascript
var a; // a contains value as undefined. undefined represents a declared variable that is not defined.
```

4. Number: is a primitive type that represents both integer and floating point numbers.

```javascript
let a = 6;
let b = 7.12; 
```

5. BigInt: is a primitive type to represent whole numbers greater than 2<sup>53</sup> - 1.

```javascript
let a = 123n; // n at the end represent BigInt
```

6. String: is a primitive type that represents a series of characters.

```javascript
let a = "Hello";
```

7. Symbol: is a primitive type whose instances are unique and immutable.

```javascript
let s1 = Symbol("foo");
let s2 = Symbol("foo");
console.log(s1 === s2); // false. Symbols produce unique value each time.
```

Anything that is not of primitive type is considered to be an object type in JavaScript.

JavaScript is a dynamically typed language.

```javascript
let a = 10;
console.log(typeof a); // "number"
a = "Joby";
console.log(typeof a); // "string"
```

Literals are used to represent values in JavaScript.

```javascript
let a = ["Apple", "Banana"]; // Array literal
let b = true; // Boolean literal
let c = 23; // Numeric literal
let d = "Hello"; // String literal
let e = { name: "Joby" }; // Object literal
```
