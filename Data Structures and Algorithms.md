## The Big O Notation

We use Big O notation to describe the performance of an algorithm. It represents run time complexity of an algorithm. It helps to find if an algorithm is scalable or not.

It is associated with Data Structures because performance of an algorithm changes based on the data structure we use. Eg: It is very to read an item from array, but costly to do inserting an item. On the other hand, inserting an element is easy in linkedlist, but reading an item is difficult.

Consider following function in Java:

```java
public void printFirstElement(int[] numbers) {
    System.out.println(numbers[0]);
}
```

Irrespective of the size of array, the time taken to print the value of first element will be a constant. Therefore, the Big O will be __O(1)__.

Consider following code snippet:

```java
public void log(int[] numbers) {
    for (int i = 0; i < numbers.length; i++) {
        System.out.println(numbers[i]);
    }
}
```

As the input size increases, the algorithm time increases linearly. In this case Big O is __O(n)__, where `n` is the input size.

Consider following code snippet:

```java
public void log(int[] numbers) {
    for (int i = 0; i < numbers.length; i++) {
        for (int j = 0; j < numbers.length; j++) {
            System.out.println(numbers[i] + " " + numbers[j]);
        }
    }
}
```

As the input size increases, the number of operations increases quadratically. For input size of n, there will be n<sup>2</sup> operations. Therefore Big O is __O(n<sup>2</sup>)__.

We have logarithmic Big O when the the problem is reduced to half in each step. Eg: Binary Search. They have Big O of __O(log n)__.

The opposite of logarithmic growth is exponential growth which __O(2<sup>n</sup>)__.

