# Dynamic Programming

## Table of Contents

* [Introduction](#introduction)
* [Dynamic vs Brute force](#terminology)
* [The funny table thing](#terminology)
* [Recursion and dynamic programming](#terminology)
* [External references](#external-references)

## Introduction

Dynamic programming is a simple method of finding optimal (best) solutions to complex problems. It does this by deriving the optimal solution from optimal solutions to simpler versions of the same problem.

### Typical problems

Dynamic programming can be applied to these *classic* programming problems.

#### Travelling salesman

A travelling salesman has to visit several cities, then return home. It doesn't matter what order she visits the cities in, she just wants to find the shortest possible journey.

![gif visualisation of traveling salesman problem](https://upload.wikimedia.org/wikipedia/commons/2/23/Nearestneighbor.gif)
> [Nearest Neighbour algorithm for a TSP with 7 cities - Wikipedia](https://en.wikipedia.org/wiki/Travelling_salesman_problem#/media/File:Nearestneighbor.gif) licensed under CC BY-SA 3.0

#### Knapsack

A traveller has a knapsack with limited (weight) capacity. She can take a variety of items each with a different weight and cash values. She must work out the highest cash value combination of items she can fit in her knapsack.
[a version of the knapscap problem](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/Knapsack.svg/486px-Knapsack.svg.png)
>[Knapsack problem - Wikipedia](https://en.wikipedia.org/wiki/Knapsack_problem#/media/File:Knapsack.svg) licensed under CC BY-SA 2.5

### Brute force solutions

We could attempt to solve this problems using *brute force*. This involves finding every possible solution and comparing them all, to find the best. For simple versions of the problem (like a Knapsack problem with only a few items) this is not so bad. But as the options grow the number of solutions quickly become too large to compute efficiently. For instance, there are over 3 million possible routes to a travelling salesman problem with 10 cities and nearly 500 million for 12 cities.

We need a better approach for complex problems.

###



## External references
- [Travelling salesman](https://simple.wikipedia.org/wiki/Travelling_salesman_problem)
- [Knapsack problem](https://en.wikipedia.org/wiki/Knapsack_problem)
