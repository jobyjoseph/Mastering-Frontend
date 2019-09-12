1. [Variables](#variables)
2. [Data Types](#data-types)
3. [Conditionals](#conditionals)

## Variables

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

Kotlin does not allow a _nullable_ variable to be treated like a _non-nullable_ variable.

```kotlin
val name: String? = null;
println(name.toUpperCase()); // Error: Only safe (?.) or non-null asserted (!!.) calls are allowed on a nullable receiver of type String?
```

## Data Types

In order to use numerical data, there are 6 data types in Kotlin.

```kotlin
var a : Byte = 5;
var b : Short = 50;
var c : Int = 500;
var d : Long = 5000;
var e : Float = 50000.10f;
var f : Double = 500000.00;
```

## Conditionals

_if-else statement_ can be used to implement conditional logic.

```kotlin
if( a == 10) {
    println("I am in if block");
} else {
    println("I am in else block");
}
```

Multiple conditions can be represented using _else if_.

```kotlin
if( a > 80) {
    println("Excellent");
} else if( a > 60 ){
    println("Very Good");
} else {
    println("Need to improve");
}
```

_Conditional Expressions_ allow to assign values conditionally to a variable. Kotlin does not support ternary operator.

```kotlin
val a = 10;

val result = if( a > 30 ) {
    "You passed"
} else {
    "You failed"
}

println(result); // "You failed"
```

`when` expression reduces the complexity of a conditional statement.

```kotlin
val a = 10;
val result = when {
    a > 80 ->   "You scored good marks"
    a > 40 ->   "You passed"
    else -> "You failed"
}
println(result); // "You failed"
```

Kotlin’s conditionals highlight one of its more powerful features, _smart casting_.

```kotlin
val name: String? = null;
if (name != null) {
    println(name.toUpperCase()); // Kotlin understood that we are doing a null check. So it is not throwing error in this line.
} 
// If the null check was not there we have to use name?.toUpperCase()
```

## References

Learn Kotlin Programming Language - https://developer.android.com/kotlin/learn
