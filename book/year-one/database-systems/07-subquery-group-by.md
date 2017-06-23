# Group By and Subqueries

## Table of Contents

* [Introduction](#introduction)
* [Group by](#group-by)
* [Subqueries](#subqueries)
* [Resources](#resources)

## Introduction

Group by statements and subqueries allow us to create more complex SQL queries that answer more complex questions.

## Group by

The GROUP BY statement used to divide query results into chunks / groups by values in a specific column. Group By is often used with aggregate functions (COUNT, MAX, MIN, SUM, AVG) to find, for instance, the total value of all the orders for each each customer. The SQL looks like this:

```
SELECT CustomerID, SUM(OrderValue) as "Total order value"
FROM orders
GROUP BY CustomerID`
```

## Subqueries

A Subquery (aka Inner query or Nested query) is a query within another SQL query and embedded within the WHERE clause.

A subquery is used to restrict the data used in the main query.

Subqueries can be used with the SELECT, INSERT, UPDATE, and DELETE statements along with the operators like =, <, >, >=, <=, IN, BETWEEN, etc.

For example, this query will get all customer who earn more than 45000.

```
SELECT * FROM CUSTOMERS
WHERE ID IN
(SELECT ID FROM CUSTOMERS
WHERE SALARY > 45000)
```
Subqueries must follow these rules:
1. Subqueries must be enclosed within parentheses.
2. A subquery can have only one column in the SELECT clause, unless multiple columns are in the main query for the subquery to compare its selected columns.
3. An ORDER BY command cannot be used in a subquery, although the main query can use an ORDER BY. The GROUP BY command can be used to perform the same function as the ORDER BY in a subquery.
4. Subqueries that return more than one row can only be used with multiple value operators such as the IN operator.
5. The SELECT list cannot include any references to values that evaluate to a BLOB, ARRAY, CLOB, or NCLOB.
6. A subquery cannot be immediately enclosed in a set function.
7. The BETWEEN operator cannot be used with a subquery. However, the BETWEEN operator can be used within the subquery.

## Resources:

* [Group by](https://www.w3schools.com/sql/sql_groupby.asp)
* [Tutorial point - SQL Sub queries](https://www.tutorialspoint.com/sql/sql-sub-queries.htm)
