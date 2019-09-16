## Contents

- [The Big O Notation](#the-big-o-notation)
- [Arrays](#arrays)

## The Big O Notation

We use Big O notation to describe the performance of an algorithm. It represents run time complexity of an algorithm. It helps to find if an algorithm is scalable or not.

It is associated with Data Structures because performance of an algorithm changes based on the data structure we use. Eg: It is very easy to read an item from array, but costly to insert an item. On the other hand, inserting an element is easy in linkedlist, but reading an item is costly.

Consider following function in Java:

```java
public void printFirstElement(int[] numbers) {
    System.out.println(numbers[0]);
}
```

Irrespective of the input size(_n_) of the array, the time taken to print the value of first element will be a __constant__. Therefore, the Big O will be __O(1)__.

Consider following code snippet:

```java
public void log(int[] numbers) {
    for (int i = 0; i < numbers.length; i++) {
        System.out.println(numbers[i]);
    }
}
```

As the input size(_n_) increases, the algorithm time increases __linearly__. In this case Big O is __O(n)__.

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

As the input size increases, the number of operations increases __quadratically__. For input size of n, there will be n<sup>2</sup> operations. Therefore Big O is __O(n<sup>2</sup>)__.

We have logarithmic Big O when the the problem is reduced to half in each step. Eg: Binary Search. They have Big O of __O(log n)__.

The opposite of logarithmic growth is exponential growth which __O(2<sup>n</sup>)__.

## Arrays

Array is a data structure. It is available in most of the programming languages. It is used to store a list of items. These items are stored __sequentially__ in memory.

### Lookup Item

Since arrays store its item sequentially in memory, the time taken to get an item by its index is a constant.

```java
int arrayLookup(int index, int[] arr) {
    return arr[index];
}
```

In the above function, what ever index value we give, the time taken is a constant. Therefore, the Big O for array lookup is __O(1)__.

### Insert Item

In Java, the size of an array is static. We need to mention the size of array while declaring it. In order to insert an item to an array, we might need to resize the array.

```java
void insert(int item) {
    if( count == items.length ){ // count tracks the number of elements in the array, items is an actual array
        int[] newItems = new int[count*2]; // Increasing the size of array
        for (int i = 0; i < count; i++) {
            newItems[i] = items[i];
        }
        items = newItems;
    }
    items[count++] = item;
}
```

The run time of this function increases as the input size of `items` array increases. Therefore, the Big O for inserting an item to an array is __O(n)__.

### Delete Item

If we are deleting an array item from last, the run time is smallest. It will always be a constant, resulting in Big O of __O(1)__. But that is the best case. We need to consider the worst case while calculating Big O.

To delete the first item, we need to shift the entire elements after first item one place to left.

```java
void removeAt(int index) {
    if( index > 0 && index < count ) { // 'count' is the number of elements in 'items' array.
        for(int i = index; i < count - 1; i++) {
            items[i] = items[i + 1];
        }
    } else {
        throw new IllegalArgumentException();
    }
    count--;
}
```

The Big O for deleting an item from an array is __O(n)__.

### Search Item

In an array, if we need to search for an item, we need to loop through the array.

```java
int indexOf(int item) {
    for(int i = 0; i < count; i++) {
        if (items[i] == item) {
            return i;
        }
    }
    return -1;
}
```

As the size of the array increases, the time to find an item increases. Therefore the Big O to search an array item is __O(n)__.

## LinkedList

LinkedList is a data structure. It is used to store a sequence of elements. It can grow or shrink automatically.

### Lookup Item

If we need to find the i<sup>th</sup> element in a linkedlist, we need to start from the head and loop through. Therefore, the Big O for linkedlist lookup is __O(n)__.

### Search Item

If we need to search for an item, we need to start checking from head of linkedlist. That makes the Big O of operation to __O(n)__.

### Insert Item

Inserting an item in the end is an _O(1)_ operation. Inserting in the beginning is an _O(1)_ operation. Inserting in the middle is an _O(n)_ operation. So considering the worst case, insertion in Linkedlist is an __O(n)__ operation.
