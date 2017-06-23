# Tables, Fields, Primary Keys

## Table of Contents

* [Introduction](#introduction)
* [Basic terminology](#basic-terminology)
* [Chapter heading](#chapter-heading)
* [Resources](#resources)

## Introduction

This chapter is all about design and creating database tables. It describes how tables can be related to one another and lists some useful SQL commands to build a database.

## Basic terminology

- **Table:** A table is responsible for storing data in the database. Database tables consist of rows and columns.
- **Field:** A field is where your data lives, each field will have defined with a data type.
- **Relationship:** Two or more tables containing related data.
- **Record:**  A row of fields.
- **Primary Key:** Uniquely identifies each record in a database table. E.g. your Email or your National Insurance Number.
- **Foreign Key:**  Used to link two tables together.

## Structuring databases

### Basic structure

Relational databases are organised into *tables*. *Tables* can be visualised as a spreadsheet, the column headings tell you the type of information contained (e.g. First Name, Date of Birth, etc...).

In databases, these columns are referred to as *fields*. Each *row* in your database represents a *record*. For instance, in a database of employees, each *row* will contain the record of a single employee. The *fields* will include information about that employee (name, email, salary, etc...).

### Primary Keys

Each *row* in the *table* should have a *primary key*. A *primary key* must be unique, as it must be able to identify one row (and one row only) in the table.

In our employees table, using "name" as a *primary key* would be a bad idea, as people might have the same name (there might be lots of John Smiths). We could instead use finger prints or DNA (these are unique to each individual), however this is a bit impractical (imagine scanning a fingerprint every time you wanted to query the database).

In most cases the *primary key field* will be given a unique number. Most SQL database systems can generate a unique number for you.

### Relationships

Tables can be linked so one table can access the data in another. We can illustrate this idea by looking at the Product table in the example [Northwind database](https://northwinddatabase.codeplex.com/). The product table includes these fields:

```
+-----------------+
| Product fields  |
+-----------------+
| ProductID       |
| ProductName     |
| SupplierID      |  // Foreign key
| UnitPrice       |
| etc....         |
+-----------------+
```

Each product has a supplier. We could store all the supplier data as extra fields in the product table (e.g. Supplier name, supplier address, etc...). However, in this example the Products table only includes the SupplierID field. SupplierID is a *primary key* in the Supplier table. Using the SupplierID, the product table can uniquely identify a supplier and access all the data in the supplier table. This is why (in the Products table) SupplierID is a *foreign key* (it is a key to another, foreign, table).

```
+-----------------+
| Supplier fields |
+-----------------+
| SupplierID      |  // Primary key
| CompanyName     |
| ContactName     |
| Post code       |
| etc....         |
+-----------------+
```

Using *foreign keys* in this way means, if supplier details change (e.g. a supplier moves address), we only need to update the supplier table. We do not need to find all the relevant products in the products table change the address for each one.

## Using DDL to build tables in SQL

The commands below detail the process of building a database from the command line. [PHPMyAdmin](https://www.phpmyadmin.net/) (and other DBMS) allow you to design the database through a GUI.

* Create a new database:
`CREATE DATABASE [database_name]`

* Use a database: `USE [database_name]`

* Create a table: `CREATE TABLE [table_name] ( [column_definitions] ) `
  - For example:
```
CREATE TABLE employees (
    id INTEGER PRIMARY KEY,
    first_name VARCHAR(50) NULL,
    last_name VARCHAR(75) NOT NULL,
    dateofbirth DATE NULL
);
```
> When creating a table we must include the data type for each field. See chapter 3 for more information.

* Delete a table `DROP TABLE [table_name]`

* Alter a table (e.g. add a new field)
`ALTER TABLE employee
ADD salary money null `

## Resources:

* [Northwind database](https://northwinddatabase.codeplex.com/)
* [W3 schools - DDL section](https://www.w3schools.com/sql/sql_create_db.asp)
* [Quack It tutorial - make a database](https://www.quackit.com/database/tutorial/creating_a_database.cfm)
* [SQL Data Definition Language](http://www.code2learn.com/2012/06/sql-data-definition-language-ddl.html)
