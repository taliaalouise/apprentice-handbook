# Sample Code

## Table of Contents

* [Sorting Algorithms](#sorting-algorithms)
  1. [Bubble Sort](#bubble-sort)
  1. [Selection Sort](#selection-sort)
  1. [Insertion Sort](#insertion-sort)
* [Searching Algorithms](#searching-algorithms)
  1. [Linear Search](#linear-search)
  1. [Binary Search](#binary-search)

## Sorting Algorithms

### Bubble Sort

```java
public class Main {
  public static void main(String[] args) {
    int[] arr = {4, 3, 2, 1};
    bubbleSort(arr);
    // Array is now sorted in ascending order.
  }

  private static void bubbleSort(int[] arr) {
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
}
```

### Selection Sort

```java
public class Main {
  public static void main(String[] args) {
    int[] arr = {4, 3, 2, 1};
    selectionSort(arr);
    // Array is now sorted in ascending order!
  }

  private static void selectionSort(int[] arr) {
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
}
```

### Insertion Sort

```java
public class Main {
  public static void main(String[] args) {
    int[] arr = {4, 3, 2, 1};
    insertionSort(arr);
    // Array is now sorted in ascending order!
  }

  private static void insertionSort(int[] arr) {
    int minIdx = 0;

    for (int i = 0; i < arr.length; i++) {
      for (int j = i; j < arr.length; j++) {
        if (arr[j] < arr[minIdx]) minIdx = j;
      }

      int swap = arr[i];
      arr[i] = arr[minIdx];
      arr[minIdx] = swap;
      minIdx = i + 1;
    }
  }
}
```

## Searching Algorithms

### Linear Search

```java
public class Main {
  public static void main(String[] args) {
    int[] arr = {4, 3, 2, 1};
    boolean found = linearSearch(3, arr);
  }

  private static boolean linearSearch(int n, int[] arr) {
    for (int element : arr) {
      if (n == element) {
        return true;
      }
    }
    return false;
  }
}
```

### Binary Search

```java
public class Main {
  public static void main(String[] args) {
    int[] arr = {4, 3, 2, 1};
    boolean found = binarySearch(3, arr);
  }

  private static boolean binarySearch(int n, int[] arr) {
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
}
```
