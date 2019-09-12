Variable declaration and initialization in Java:

```java
int age = 30;
```

Types in Java are categorized to _primitive_ and _reference_ types.

Primitive types in Java are:
- byte - 1 byte
- short - 2 bytes
- int - 4 bytes
- long - 8 bytes
- float - 4 bytes
- double - 8 bytes
- char - 2 bytes
- boolean - 1 byte

We can use _ to make numbers more readable.

```java
int visitCount = 123_888_901;
```

We need to add `L` for a long integer in Java. Without `L`, Java compiler treats the number as integer.

```java
long visitCount = 3_012_781_903L;
```

We need to add `F` to represent float type.

```java
float price = 10.99F;
```

## Strings

Strings in Java are created using `String` class.

```java
String message = "Hello World!!";
```

## Arrays

```java
// Declaring an integer array
int[] number = new int[];
```
