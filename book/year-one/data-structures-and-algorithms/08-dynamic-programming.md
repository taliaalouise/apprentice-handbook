# Dynamic Programming

## Table of Contents

* [Introduction](#introduction)
* [Typical problems](#typical-problems)
* [Brute force](#brute-force)
* [The dynamic approach](#the-dynamic-approach)
* [External references](#external-references)

## Introduction

Dynamic programming is a simple method of finding optimal (best) solutions to complex problems. It does this by deriving the optimal solution from solutions to simpler versions of the same problem.

## Typical problems

Dynamic programming can be applied to these *classic* programming problems.

### Travelling salesman

A travelling salesman has to visit several cities, then return home. It doesn't matter what order she visits the cities in, she just wants to find the shortest possible journey that includes all cities.

![gif visualisation of traveling salesman problem](https://upload.wikimedia.org/wikipedia/commons/2/23/Nearestneighbor.gif)
> [Nearest Neighbour algorithm for a TSP with 7 cities - Wikipedia](https://en.wikipedia.org/wiki/Travelling_salesman_problem#/media/File:Nearestneighbor.gif) licensed under CC BY-SA 3.0

### Knapsack

A traveller has a knapsack with limited (weight) capacity. She can take a variety of items each with a different weight and cash values. She must work out the highest cash value combination of items she can fit in her knapsack.
![a version of the knapscap problem](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/Knapsack.svg/486px-Knapsack.svg.png)
>[Knapsack problem - Wikipedia](https://en.wikipedia.org/wiki/Knapsack_problem#/media/File:Knapsack.svg) licensed under CC BY-SA 2.5

## Brute force

We could attempt to solve these problems using *brute force*. This involves finding every possible solution and comparing them all, to find the best. For simple versions of the problem (like a Knapsack problem with only a few items) this is not so bad. But as the options grow the number of solutions quickly become too large to compute efficiently. For instance, there are over 3 million possible routes to a travelling salesman problem with 10 cities and nearly 500 million for 12 cities.

We need a better approach for complex problems.

## The Dynamic approach

The general idea of Dyanmic program is to find a solution the simplest version of the problem and then work your way up to the more complex version you actually want to solve. Take the knapsack problem. The simplest version of any knapsack problem is a situation where only one of the items is available and you have a bag with only 1kg capacity. We can then slowly add more weight capacity to our bag and make more items available until we scale up to the actual problem we want to solve.

### Example knapsack problem

In this knapsack problem we have a bag with **6kg capacity** and the following items:

Item number       |1            | 2          |3            |4           |5
------------------|-------------|------------|-------------|------------|-----------
Weight (kg)       |3            |2           |1            |4           |5 
Value (£)         |25           |20          |15           |40          |50

### Solving this knapsack problem a dynamic table

We can record the process of scaling up from simple to complex using the table below. 

We can work out the solution row by row, column by column to find the best solution in each case. Look at the "Item 1 only" row. *Item 1* has a 3kg weight and is worth £25. Work your way along the row. We know we can only take *Item 1* when we have a 3kg bag, which will give us a solution of the value £25. As we increase the weigth capacity we cannot increase the value of the solution, as in this row we only have *Item 1* available.

Work your way along the next row, "Item 1 & 2 only". Now we have the option to take *Item 1* or *Item 2*, or both. *Item 2* (only 2kg) is lighter than *Item 1*, so we can take it when we have a 2kg bag. We can record its value (£20) in the "2kg bag" column. In the "3kg bag" column, we don't have enough weight to take both *Item 1* and *Item 2*, we must choose. Naturally, the best solution is to take *Item 1* as it is worth more. When we have a 5kg bag, we can take both *Item 1* and *Item 2* and therefore we can combine there values to make £45.

We can work our way along the table, considering the best possible solution for each combination of items with bags of different capacities.

Dynamic table        |0kg bag      |1kg bag     |2kg bag      |3kg bag      |4kg bag   |5kg bag    |6kg bag
---------------------|-------------|------------|-------------|-------------|----------|-----------|-----------
No items available   |0            |0           |0            |0            |0         |0          |0
Item 1 only          |0            |0           |0            |25           |25        |25         |25
Item 1 & 2 only      |0            |0           |20           |25           |25        |45         |45
Item 1, 2 & 3 only   |0            |15          |20           |35           |40        |45         |60
Item 1, 2, 3 & 4 only|0            |15          |20           |35           |40        |55         |60
All items 1 to 5     |0            |15          |20           |35           |40        |55         |65

In the last cell of the table we have the problem we actually want to solve - a 6kg capacity knapsack with all 5 items to choose from. We have found the best possible solution, with a value of £65. But how do we know which values are part of the solution? There is a  alogrithm we can follow to work this out.
1. Start at the cell with the best solution (in this case £65).
2. Move up the column until the value changes. In this case we can't move up, as the cell above is of lower value (only £60). We now know that *Item 5* must be part of the solution (without it, we couldn't find a better solution).
3. We also know that *Item 5* has a weight of 5kg. If our bag has a 6kg capacity and we must have *Item 5* in the bag, we only have 1kg left to play with.
4. Move along to the *remaining capacity* column (1kg in this case). Work you way up from the bottom of the column until the value changes. Here we can't move past row "Item 1, 2, & 3 only". This means we must include *Item 3* in the solution, as without it the solution is of a lower value.
5. *Item 3* uses up all our remaining capacity (1kg) so we can't add any more items.
6. We now the best solution is *Item 5* and *Item 3*: £50 + £15 = £65.

### Copy down from the row above to save time

Filling in the table will always find the optimal (best) solution. But it can be labourious. There are some shortcuts we can take.

As we move down the rows, we add one new item each time. When adding a new item, we can copy the values from the row above until we reach the **first column that is equal weight to the new item**. 

Take the jump from Items 1-3 to Items 1-4. *Item 4* is 4kg so we know we can copy down up to the "4kg bag" column. 

Excerpt of above     |0kg bag      |1kg bag     |2kg bag      |3kg bag      |4kg bag             |5kg bag    |6kg bag
---------------------|-------------|------------|-------------|-------------|--------------------|-----------|-----------
Item 1, 2 & 3 only   |0            |15          |20           |35           |40                  |45         |60
Item 1, 2, 3 & 4 only|0 [COPY]     |15 [COPY]   |20 [COPY]    |35 [COPY]    |...[work from here] |           |

This makes sense if we consider the fact that a 4kg item can only come into consideration when we have a bag with a capcity of at leasgt 4kg. Up to that point our optimal solution cannot change form the row above.

## Recursive approach - the real power of dynamic programming

As we move through the table and work out the best solution for each case we are sort of doing *brute force* in our head (imagine how you would work out the best solution in a table with 100s of rows and columns!!). We need a simple way to find the value for any cell, based on previous cells. This would really speed up the process of completing the table and find the best approach.


## External references
- [Travelling salesman](https://simple.wikipedia.org/wiki/Travelling_salesman_problem)
- [Knapsack problem](https://en.wikipedia.org/wiki/Knapsack_problem)
