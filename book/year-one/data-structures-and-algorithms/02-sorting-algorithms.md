# Sorting Algorithms

## Table of Contents

* [Introduction](#introduction)
* [Bubble sort](#bubble-sort)
* [Selection sort](#selection-sort)
* [Insertion sort](#insertion-sort)

## Introduction

In computer science a sorting algorithm is an algorithm that puts elements of a list in a certain order. We could say we want to sort it in one of two ways: **ascending** or **descending**.

```js
[0, 1, 2, 4, 5] // Ascending order!
[5, 4, 2, 1, 0] // Descending order!
```

Below each title you will find the [complexity](07-big-o-notation.md). They are there for future reference only.

## Bubble Sort

**Complexity:** `Time: O(n^2), Space: O(1)`

Compares an element to its neighbor, if the element is larger that its neighbor, they swap places. The largest elements “bubble up” to the end with each pass of the loop.

Bubble Sort in action:

![gif explaining bubble sort](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif?1495630103933)

Example in Java:

```java
//        Sort a fixed length array using Bubble Sort:

int[] arr = {4, 3, 2, 1};

public static void bubbleSort(int[] arr) {
  boolean sorted;

  do {
    sorted = true;
    for (int i = 0; i < arr.length-1; i++) {
      int current = arr[i];
      int next = arr[i+1];

      if (current > next) {
        sorted = false;
        arr[i] = next;
        arr[i+1] = current;
      }
    }
  } while (!sorted);
}
```

## Selection Sort

**Complexity**: `Time: O(n^2), Space: O(n)`

Compares an element against all the elements of the array until it finds the smallest, then they swap places. Small elements get pushed to the beginning with each pass of the loop.

Selection Sort in action:

![gif explaining selection sort](http://www.codingconnect.net/wp-content/uploads/2016/09/Selection-Sort.gif)

Example in Java:

```java
// Sort a fixed length array using Selection Sort:

int[] arr = {4, 3, 2, 1};

public static void selectionSort(int[] arr) {
  for (int i = 0; i < arr.length; i++) {
    int minIndex = i;

    for (int j = i; j < arr.length; j++) {
      if (arr[j] < arr[minIndex]) {
        minIndex = j;
      }
    }

    int swapped = arr[minIndex];
    arr[minIndex] = arr[i];
    arr[i] = swapped;
  }
}
```

## Insertion Sort

**Complexity:**`Time: O(n^2), Space: O(n)`

Insertion Sort in action:

![gif explaining insertion sort](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif?1495630165237)

