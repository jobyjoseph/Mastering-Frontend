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
