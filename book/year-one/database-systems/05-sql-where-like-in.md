# Where, Like, In and Logic Operators

## Table of Contents

* [Introduction](#introduction)
* [Where statements](#where-statements)
* [Logic Operators](#logic-operators)
* [Like Operator](#like-operator)
* [In Operator](#in-operator)
* [Order by](#order-by)
* [Resources](#resources)

## Introduction

Where, Like and In (alongside logic operators) are used to narrow down query results for Select, Update, and Delete statements (see Chapter 4). In this chapter will only include examples of Select statements, but all examples could be adapted for Update and Delete.

## Where statements

The Where clause is used to filter records.

`SELECT column1, column2, … FROM table_name WHERE condition;`

For example:

`SELECT * FROM Customers WHERE name='Joe Bloggs';`

## Logic Operators

Logic operators can be used to create complex conditions for use in `WHERE` statements.

### Comparison

* `=`	Equal
* `<>` (or sometimes !=)	Not equal
* `>`	Greater than
* `<`	Less than
* `>=`	Greater than or equal
* `<=`	Less than or equal to

### Truth functional
`AND` - TRUE if all the conditions separated by AND is TRUE,
`OR` - TRUE if any of the conditions separated by OR is TRUE,
`NOT` - Displays a record if the condition(s) is NOT TRUE

### Examples

Find all customers who live in Paris or London
`SELECT * FROM Customers WHERE city='Paris' or city ='London'`

Find all adult customers in Berlin
`SELECT * FROM Customers WHERE city='Berlin' and age >= 18;`

Find all customers who don't live in London
`SELECT * FROM Customers WHERE city !='London'`

## Like operator

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

Typical Wildcards used with LIKE
% - The percent sign represents zero, one, or multiple characters
_ - The underscore represents a single character

### Examples

Find all customers who's name begins with A
`SELECT * FROM Customers WHERE name like 'A%';`

Find all customers who live in N17
`SELECT * FROM Customers WHERE postcode like 'N17%';`

Find all customers who live in a city which begins with B and is 6 letters long (Berlin, Bruges, Beirut, etc...)
`SELECT * FROM Customers WHERE name like 'B_____';`

## In operator

The IN operator allows you to specify multiple values in a WHERE clause.

`SELECT column_name(s) FROM table_name
WHERE column_name IN (value1, value2, ...)`

### Example

Find customers all customers in Germany, France, or UK.

`SELECT * FROM Customers WHERE Country IN ('Germany', 'France', 'UK');`

## Order by

The `ORDER BY` keyword is used to sort the result-set in ascending or descending order.

`SELECT column1, column2, … FROM table_name ORDER BY column1, column2, ... ASC|DESC;`

### Example

List customer by name in alphabetical order

`SELECT * FROM Customers ORDER BY name ASC;`s


## Resources:

* [W3 Schools: Where statements](https://www.w3schools.com/sql/sql_where.asp)
* [W3 Schools: Like Operator](https://www.w3schools.com/sql/sql_like.asp)
* [W3 Schools: In Operator](https://www.w3schools.com/sql/sql_in.asp)
* [W3 Schools: Order by](https://www.w3schools.com/sql/sql_orderby.asp)
