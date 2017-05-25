# Recursion

## What is recursion?

A function that calls itself.

## Why use recursion?

Recursion works very similarly to loops in programming.

## Examples and applications

**The Handshake Problem** - There are `n` people in a room. If each person shakes hands once with every other person, what is the total number of handshakes?

`10 people -> 9 + 8 + 7 + 6 + 5 + 4 + 3 + 2 + 1 = 45 handshakes`

Example in Java:

```java
// Handshake problem in code

int handshakes(int n) {
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
