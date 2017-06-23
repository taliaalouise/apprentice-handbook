# Joins, Unions and views

## Table of Contents

* [Introduction](#introduction)
* [Joins](#joins)
* [Unions](#unions)
* [Views](#views)
* [Resources](#resources)

## Introduction

In chapter 2 we discussed relationships between tables. We said primary keys and foreign keys can be used to link tables together.

Joins and Unions allow us to combine two or more tables to make one larger table. This is how we can take primary / foreign key relationships and use them in practice.

Views allow us to save SQL queries to use them again later.

## Joins

A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

Different Types of the JOINs in SQL:
- (INNER) JOIN,
- LEFT (OUTER) JOIN
- RIGHT (OUTER) JOIN,
- FULL (OUTER) JOIN

All joins have this syntax

```
SELECT Table1.columnX, Table2.columnY,
FROM Table1
[TYPE] JOIN Table2 ON Table1.columnJ=Table2.columnR;
```

As we are referring to two tables we need to use the TableName.ColumnName notation to be really clear about what we want from where (this avoids any confusion about column with the same name in different tables).

### Joins often use primary key and foreign key

You don't have to join tables with primary / foriegn keys (you can use any columns to make a join). However, in practice this is often sensible to use primary and foreign keys as they allow us to uniquely identify matching items in different tables.

In the inner join example code below, Orders.CustomerID = Customers.CustomerID, is an instance of a primary / foreign key join.

### (INNER) JOIN:

Returns records that have matching values in both tables

![inner join venn diagram](https://www.w3schools.com/sql/img_innerjoin.gif)

Select all orders and find the customer name (from a different table):

```
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```



### LEFT (OUTER) JOIN:

Return all records from the left table, and the matched records from the right table

![left join venn diagram](https://www.w3schools.com/sql/img_leftjoin.gif)

Select all customers, and any orders they might have:

```
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```


### RIGHT (OUTER) JOIN:

Return all records from the right table, and the matched records from the left table

![right join venn diagram](https://www.w3schools.com/sql/img_rightjoin.gif)

Select all employees, and any orders they might have have placed:

```
SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;
```
### FULL (OUTER) JOIN:

Return all records when there is a match in either left or right table.

![full join venn diagram](https://www.w3schools.com/sql/img_fulljoin.gif)

Select all customers and all orders:

```
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```

## Unions

The UNION operator is used to combine the result-set of two or more SELECT statements.

- Each SELECT statement within UNION must have the same number of columns
- The columns must also have similar data types, ‘similar’ depending on you DBMS (MySQL, SQL Server, Oracle or else)
- The columns in each SELECT statement must also be in the same order

The UNION operator selects only distinct values by default.

```
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

For example, this will find all distinct German cities

```
SELECT City, Country FROM Customers
WHERE Country='Germany'
UNION
SELECT City, Country FROM Suppliers
WHERE Country='Germany'
ORDER BY City;
```

To allow duplicate values, use UNION ALL:

```
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```

## Views

View statements create virtual tables based on the results of an SQL statement. They are virtual because the database doesn't actually copy all the data and save it somewhere. A view is a bit like an method in Java, you are saving an SQL query to be used again later.

In practice, views often run faster than the original SQL query, as databases can cache the results of a View for speedy access at a later time.

Views are also helpful as they can make your SQL queries easier to read, by hiding some of the details.

To create a view

```
CREATE VIEW view_name AS SELECT column1, column2, ...
FROM table_name WHERE condition;
```

To query a view

`SELECT * FROM view_name;`

To delete a view

`DROP VIEW view_name;`

## Resources:

* [W3 Schools - SQL Joins](https://www.w3schools.com/sql/sql_join.asp)
* [W3 Schools - SQL Union operator](https://www.w3schools.com/sql/sql_union.asp)
* [W3 Schools - SQL Views](https://www.w3schools.com/sql/sql_view.asp)
