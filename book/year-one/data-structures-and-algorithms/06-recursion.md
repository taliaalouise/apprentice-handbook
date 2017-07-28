# Recursion

## Table of Contents

* [What is recursion?](#what-is-recursion)
   * [Base case](#base-case)
* [Why use recursion?](#why-use-recursion)
* [Examples and applications](#examples-and-applications)
* [External Resources](#external-resources)

## What is recursion?

A function that calls itself. 

### Base case

Recursive functions usually have a base case. This is the point at which the function stops calling itself, and starts returning some value. Without a base case a recursive function might run forever in an infinite loop.

If you imagine a recursive function for opening Russian (Matryoshka) dolls. We want to open the dolls until we reach the smallest doll. The smallest doll would be the *base case*.

```
// Pseudocode
public openDolls(doll) {
   if (doll == smallest) {
      return doll;      // This is the base case. We can't find a smaller doll
   } else {
      smallerDoll = doll - 1;
      return openDolls(smallerDoll);      // Here the function calls itself. The recursive part.
   }
}
```
![Russian matryoshka dolls](https://upload.wikimedia.org/wikipedia/commons/3/3d/First_matryoshka_museum_doll_open.jpg)
>[The original matryoshka set by Zvyozdochkin and Malyutin, 1892](https://en.wikipedia.org/wiki/Matryoshka_doll#/media/File:First_matryoshka_museum_doll_open.jpg) - public domain

## Why use recursion?

Recursion works very similarly to loops in programming. In fact, we can write any recursive function with a loop, or vice versa. 

Recursion is sometimes preferred because it usually requires less code and is therefore considered more *elegant*. Iteration (loops) is sometimes preferred as it usually uses less memory and therefore favours *performance*.


## Examples and applications

**The Handshake Problem** - There are `n` people in a room. If each person shakes hands once with every other person, what is the total number of handshakes?

`10 people -> 9 + 8 + 7 + 6 + 5 + 4 + 3 + 2 + 1 = 45 handshakes`

Example in Java:

```java
// Handshake problem in code

public static int handshakes(int n) {
   if (n = 2) {
      return 1;
   } else {
      return (n - 1) + handshakes(n - 1);
   }
}
```
**Factorial** - Multiply a number by all the numbers below it.

`5! = 5 x 4 x 3 x 2 x 1 = 120`

Example in Java:

```java
// Calculate a factorial in code

public static int factorial(int n) {
   if (n == 1) {
      return 1;
   } else {
      return n * factorial(n - 1);
   }
}

Scanner reader = new Scanner(System.in);
System.out.println("Enter a number: ");
int userNum = reader.nextInt();
int result = factorial(userNum);
System.out.print(result);
```

**Fibonacci Sequence** - A series of numbers in which each number ( Fibonacci number ) is the sum of the two preceding numbers.

Example in Java:

```java
// Calculate the fibonacci number at a given position

public static int fibonacci(int n) {
   if (n <= 2) {
      return n - 1;
   } else {
      return fibonacci(n -  1) + fibonacci(n - 2);
   }
}

Scanner reader = new Scanner(System.in);
System.out.println("Enter a number: ");
int userNum = reader.nextInt();
int result = fibonacci(userNum);
System.out.print(result);
```
## External Resources
// TODO
