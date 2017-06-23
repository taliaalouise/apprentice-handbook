# SQL: Select, Insert, Update, and Delete

## Table of Contents

* [Introduction](#introduction)
* [Select statement](#select-statement)
* [Insert statement](#insert-statement)
* [Update statement](#update-statement)
* [Delete statement](#delete-statement)
* [Resources](#resources)

## Introduction

SQL can be used to access data within a database. This chapter describes how SQL can be used to find, insert and update data in a database.

## Select statement

Select statement can be used to access data in a database. It is a very low risk command; it just reads data and does not change the database in any way. This means, if we make a mistake with our select commands, we cannot damage the database.

`SELECT column1, column2, … FROM table_name;`

To get all columns from a table

`SELECT * FROM table_name;`

## Insert statement

Insert can be used to add a new record into a table.

`INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...);`

In this command, value1 will go into column1, value2 will go into columne2, etc...

## Update statement

Update modifies an existing record in the database. It (sorta) combines select and insert. It selects a row in the database and then inserts new values.

`UPDATE table_name SET column1 = value1, column2 = value2, ...
WHERE condition;`

Update statements require a `WHERE` clause to identify row(s) to update. We discuss `WHERE` in Chapter 5.

## Delete statements

Deletes an existing record in the database.

`DELETE FROM table_name WHERE condition;`

Delete also require a `WHERE` clause to identify row(s) to update. We discuss `WHERE` in Chapter 5.

## Resources:

* [W3 Schools - SQL Select](https://www.w3schools.com/sql/sql_select.asp)
* [W3 Schools - SQL Insert](https://www.w3schools.com/sql/sql_insert.asp)
* [W3 Schools - SQL Update](https://www.w3schools.com/sql/sql_update.asp)
