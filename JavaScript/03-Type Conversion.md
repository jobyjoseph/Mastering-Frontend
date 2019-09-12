In expressions involving numeric and string values with the + operator, JavaScript converts numeric values to strings.

```javascript
console.log(4 + "3"); // "43", not 7
```

`parseInt()` and `parseFloat()` are used to convert string to number.

```javascript
let a = "123.78hello";
console.log(parseInt(a)); // 123
console.log(parseFloat(a)); // 123.78
```
