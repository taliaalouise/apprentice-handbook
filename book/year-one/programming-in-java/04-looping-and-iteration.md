# Looping and Iteration

## Table of Contents

* [Introduction](#introduction)
* [For Loop](#for-loop)
  * [For Each Loop](#for-each-loop)
* [While Loop](#while-loop)
  * [Do While Loop](#do-while-loop)

## Introduction

Loops are one of the most important concepts in programming, along with conditional statements such as `if`. These are what allow computers to make decisions instead of doing exactly the same thing every time they are run. The most important loops to learn are the `for` and `while` loops. (The `do while` loop is also sometimes used, but **you will not need to know it for the course**)

## For loop

The `for` loop is usually used to repeat a set of actions a certain number of times. In its simplest form it is written as follows:

```java
for (int i = 0; i < numberOfTimesToRepeat; i++) {
    // code you want to repeat
}
```

* `int i = 0`: this creates a new variable `i`, and initialises it to 0. This variable is used to keep track of how many times the loop has repeated. It doesn't have to start out at 0, but most of the time it will unless you're doing *crazy maths shit*<sup>tm</sup>.
* `i < numberOfTimesToRepeat`: Every time the loop starts, the program will check this condition. If it is true, it will carry out the loop. If not, it skips past the loop or stops repeating. It can be whatever condition you want, but again, it's usually going to be `i < aNumber` unless you're doing *crazy maths shit*<sup>tm</sup>.
* `i++`: Every time the loop *ends*, the program will run this bit of code. It's almost always used to change the value of `i`, usually with `i++`, which increases `i`'s value by one.

### For Each Loop

A `for each` loop is a special type of for loop which "iterates" through an array. It works by moving through an array, and "for each" of a certain type of item, in the array, does something. For example:

```java
String[] fruits = {"Apple", "Banana", "Cucumber", "Durian"};

for (String fruit : fruits) {
    System.out.println(fruit);
}
```
would output the following:
```
Apple
Banana
Cucumber
Durian
```

So, the code goes through the entire `fruits` array, and for each time it repeats the code, `fruit` (you can call this variable whatever you want, it's best to be descriptive) is equal to whichever item in the array you are currently looking at.

## While loop

The `while` loop is usually used when you want to repeat some code, but you don't know exactly how many times you want to repeat it - you just want it to repeat again and again "while" something is true. It is written like this:

```java
while (condition) {
    // code you want to repeat
}
```

* `(condition)`: before the code in the loop runs, the program checks this condition. If it is true, it runs the code and then checks again. If it is false, it skips the code. The condition can be anything which resolves as a `boolean` value, so `x > y`, `x != 5` etc.

### Do While loop

The `do while` loop is almost exactly the same as the `while` loop, except it is **guaranteed to run at least once**, because it only checks the condition at the *end* of the loop instead of at the beginning. It is written like this:

```java
do {
    // code you want to repeat
} while (condition);
```

**note:** remember the semicolon at the end! The other two loops don't need a semicolon, but `do while` won't work properly unless you include it.
