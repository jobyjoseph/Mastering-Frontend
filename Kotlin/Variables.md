Value of variables declared using `val` cannot be changed.

```kotlin
val a = 5;
a = 6; // Error: Val cannot be reassigned
println("Value is ${a}");
```

Value of variables declared using `var` can be changed.

```kotlin
var a = 5;
a = 6;
println("Value is ${a}"); // "Value is 6"
```

Type of a variable can be mentioned while declaring.

```kotlin
var a : Int = 5;
a = "Hello"; // Type mismatch: inferred type is String but Int was expected
```

Kotlin can infer the type of a variable by the initial value assigned to it.

```kotlin
var a = "Joby"; // Now "a" is string type
println("Name is ${a.toUpperCase()}"); // "Name is JOBY"
```

Once the type of a variable is inferred, it cannot be changed.

```kotlin
var a = "Joby";
a = 10; // Error: The integer literal does not conform to the expected type String
```

Kotlin variables cannot contain `null` values by default.

```kotlin
var a; // Error: This variable must either have a type annotation or be initialized
a = 10;
```

We cannot assign `null` explicitly to a variable.

```kotlin
var a : String = null; // Error: Null can not be a value of a non-null type String
```

If we need to assign `null` to a non-null type variable, that variable should be of _nullable_ type. You can specify a variable as being _nullable_ by suffixing its type with `?`

```kotlin
var a : String? = null;
```


## References

Learn Kotlin Programming Language - https://developer.android.com/kotlin/learn
