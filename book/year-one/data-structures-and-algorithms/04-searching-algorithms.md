# Searching Algorithms

## Table of Contents

* [Introduction](#introduction)
* [Linear Search](#linear-search)
* [Binary Search](#binary-search)

## Introduction

> TODO: Write introduction.

## Linear Search

Going one by one along a list of items until you find what you're looking for.

Example in Java:

```java
int[] arr = {4, 3, 2, 1};

public static boolean linearSearch(int n, int[] arr) {
  for (int element : arr) {
    if (n == element) {
      return true;
    }
  }
  return false;
}
```

## Binary Search

Dividing sorted data into halves, discarding the unnecessary halves, until you find what you're looking for. Ex. Finding a name in a phone book.

Example in Java:

```java
int[] arr = {4, 3, 2, 1};

public static boolean binarySearch(int n, int[] arr) {
  int start = 0;
  int end = arr.length - 1;
  int middle;

  while (true) {
    middle = (start + end) / 2; // reset the middle index each time

    if (n == arr[middle]) { // if n is the middle number
      return true;
    }

    if (start == middle && middle == end) { // if n isn't in the array
      return false;
    }

    if (n < arr[middle]) {
      end = middle - 1;
    }

    if (n > arr[middle]) {
      start = middle + 1;
    }
  }
}
```



