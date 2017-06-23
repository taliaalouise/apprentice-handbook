# Introduction to database systems

## Table of Contents

* [Basic terminology](#basic-terminology)
* [SQL database systems](#sql-database-systems)
* [Resources](#resources)

## Basic terminology

- **Database:** A collection of data
- **Relational database:** A collection of data stored in related tables.
- **SQL:** Standard Query Language. A language for storing, manipulating and retrieving data in databases.
- **MySQL:** A popular Database management system, together with Oracle and Microsoft SQL Server. It’s open source.
- **No SQL:** A catch all term for any database system that does not use the SQL relational model. In practice NoSQL datases are a very diverse category

## SQL database systems

The chapters in this section cover the process of design, building, querying, and optimising SQL databases. NoSQL databases are beyond the scope of this course.

SQL databases organise data into tables. Tables can link to (relate to) each other.

SQL is a language that divides into two key sections

1. DML (Data Manipulation Language):
    * DML allows users to view, add, update and delete date.
    * Common commands include: SELECT, INSERT, UPDATE, and DELETE.
2. DDL (Data Definition Language):
    * DDL is used to set-up the and organise the a database.
    * It  is more complex DML, but still has a relatively small set of key terms: CREATE, USE, ALTER, RENAME, DROP and TRUNCATE.

These chapters also cover some more advanced topics relating to database design, data analysis, and database system management. These include:

* Entity relational models and relational models
* Funtional dependencies
* Normalisation
* Atomicity, Consistency, Isolation, and Durability (ACID)
* Security

## Resources:

* [Database tutorial - What is a database]https://www.quackit.com/database/tutorial/what_is_a_database.cfm)
