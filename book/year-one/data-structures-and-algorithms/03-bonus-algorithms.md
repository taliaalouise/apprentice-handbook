# Bonus sorting algorithms (not required)

## Quick Sort

### Complexity: `O(n log n)`

Quick sort is a divide and conquer algorithm. Quick sort first divides a large array into two smaller sub-arrays: the low elements and the high elements. Quick sort can then recursively sort the sub-arrays.

Quick sort's steps:
1. Pick an element, called a pivot, from the array.

2. Partitioning: reorder the array so that all elements with values less than the pivot come before the pivot, while all elements with values greater than the pivot come after it (equal values can go either way). After this partitioning, the pivot is in its final position. This is called the partition operation.

3. Recursively apply the above steps to the sub-array of elements with smaller values and separately to the sub-array of elements with greater values.

Quick sort in action (from [Wikipedia](https://en.wikipedia.org/wiki/Quicksort)):

![Quick Sort Gif](https://upload.wikimedia.org/wikipedia/commons/6/6a/Sorting_quicksort_anim.gif)

## Heap Sort

### Complexity: `O(n log n)`

In computer science, heap sort is a comparison-based sorting algorithm. Heap sort can be thought of as an improved selection sort.

Heap sort's steps:
1. Divides its input into a sorted and an unsorted region

2. Iteratively shrinks the unsorted region by extracting the largest element and moving that to the sorted region.

The improvement on selection sort consists of the use of a heap data structure rather than a linear-time search to find the maximum.

Heap Sort in action (from [Wikipedia](https://en.wikipedia.org/wiki/Heapsort)):

![Heap Sort Gif](https://upload.wikimedia.org/wikipedia/commons/4/4d/Heapsort-example.gif)

## Merge Sort

### Complexity: `O(n log n)`

Merge Sort is a divide and conquer algorithm that is an efficient, general-purpose, comparison-based sorting algorithm.

Merge sort's steps:

1. Divide the unsorted list into `n` sublists, each containing 1 element (a list of 1 element is considered sorted).

2. Repeatedly merge sublists to produce new sorted sublists until there is only 1 sublist remaining. This will be the sorted list.

Merge Sort in action (from [Wikipedia](https://en.wikipedia.org/wiki/Merge_sort)):

![Merge Sort Gif](https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif)

## External Resources

* [Merge Sort Video from Harvard's CS50](https://www.youtube.com/watch?v=EeQ8pwjQxTM)
