# Big-O Notation

## Table of Contents

* [Introduction](#introduction)
* [How to calculate complexity](#how-to-calculate-complexity)
* [Common complexities](#common-complexities)
* [External references](#external-references)

## Introduction

_Big-O_ notation is a relative representation of the *complexity* of an
algorithm. Now, what is *complexity*? It is how we describe how many steps our
algorithm will take to complete, depending on its input. That means that we want
a formula in which we can plug a number in, get out a -rough- estimate of how
many steps it should take.

We express complexity in the form of `O(formula)`, where formula can be a
number, a variable -like `x`, `y`, and usually `n`-, or multiple variables (but
we won't explore that here).

## How to calculate complexity

In this section we will use _code_-ish sentences to understand how we calculate
complexity. Take the following scenario:

```
I arrive home.
I greet my mom.
I go to my room.
```

If we look at how many *steps* this algorithm has, we can see they are always
the same. No matter what. There could be 50 people in the house, but we always
greet 1 person, and then we carry on to the rest of our steps. So we can
conclude there are *three*(3) steps. When we calculate _Big-O_ complexity we
call this `O(1)`, even though you would think it'd be `O(3)`. The reason we drop
to `1` from `3` is because when calculating complexity we don't really care
about being exact, it is an estimate. Whenever we find a **constant** complexity
we just write it as `O(1)`. So `O(5)`, `O(99)`, `O(500000)` are all `O(1)`.

Now for a scenario that's a little more complicated:

```
I arrive at my friend's party.
For every person at the house I:
  Greet said person.
For every possible food I find I:
  Eat a taste of said food.
I enjoy the party.
I go back home.
```

Now in this _algorithm_, there are some parts that are constant. Try to identify
them, there's three(3) of them. There also two sets of steps that vary depending
on how many **people**(`p`) and **food types**(`f`) there are. So we can say
that we will greet `p` amount of people and we'll try `f` amount of food. Try
think how you would express that in _Big-O_ with what you know so far. Here's
how me measure it:

1. `O(1 + p + f + 1 + 1)`
1. `O(3 + p + f)`
1. `O(p + f)`

There's something **very** important about this example. Notice `p` and `f` are
different. Now imagine instead of trying food, we would just greet people twice.
The result would be `O(p + p) -> O(2p)`. We said we drop constants, so this
would be `O(p)` (which is the same as `O(n)`). But because there is not the same
amount of people than there is of food (or at least we cant guarantee it)
`O(p + f)` is as much as we can simplify.

> The variable inside `O()` does **not** have to be `n`, even though it often
> is. Don't get confused if you see `O(x)`, it's the same as `O(n)`.

There's more to complexity analysis than we will describe here, refer to the
[external references](#external-references) provided.

## Common complexities

> You might also find this as _common runtimes_.

* `O(1)`: **Constant** - The algorithm will take the same amount of time no
  matter how large the input is.

* `O(log(n))`: **Logarithmic** - This is often the complexity for problems that
  involve looking things up, like finding a word in a dictionary. If the
  dictionary is twice as big, it contains twice as many words as the original
  to compare to. Looking something up will take only one step more. The
  algorithm to do lookups is simple. The word in the middle of the dictionary
  will be either before or after the term that needs to be looked up, if the
  words do not match. If it is before, the term needs to be in the second half
  of the dictionary. If it is after the word, it needs to be in the first half.
  That way, the problem space is halved with every step, until the word or
  definition is found. This is generally known as logarithmic complexity.

* `O(n)`: **Linear** - Mowing the lawn can be thought of as a problem with
  linear complexity. Mowing an area that is double the size of the original
  takes twice as long.

* `O(n²)`: **Quadratic** - Suppose you want to know which of your friends know
  each other. You have to ask each pair of friends whether they
  know each other. If you have twice as many friends as someone else, you have
  to ask four times as many questions to figure out who everyone knows.
  Problems that take four times as long when the size of the problem doubles
  are said to have quadratic complexity.

> Most examples are taken from [wikipedia](https://goo.gl/C07tL8)

Big-O Graph, from [Big O Cheatsheet](http://bigocheatsheet.com/):

![Big O Notation Graph](https://github.com/ada-students/apprentice-handbook/blob/master/book/assets/bigo_graph.png?raw=true)

## External references

* [Big-O Cheatsheet](http://bigocheatsheet.com/)
* [A Gentle Introduction to Algorithm Complexity Analysis](http://discrete.gr/complexity/)
