# Funcational dependencies and Normalization

## Table of Contents

* [Introduction](#introduction)
* [Functional dependencies](#functional-dependencies)
* [Anomalies](#anomalies)
* [Normalization](#normalization)
* [Resources](#resources)

## Introduction

This chapter deals with functional dependencies, anomalies, and normalization. These tools can be used to understand, analyse, and improve a database.

## Functional dependencies

A Functional dependency is a relationship between attributes. Attributes are functionally dependent when, given the value of one attribute, we can obtain the value of another attribute.

For example, if we know a customer's account number, we can obtain customer address, balance etc. This means that the customer address and balance is functionally dependent on customer account number.

### Advantages of Functional Dependency:
* Functional Dependency avoids repeated data at multiple locations in same database.
* It maintains the quality of data in database.
* It allows clearly defined meanings and constraints of databases.

### Disadvantages of Functional Dependency:
* They need to be implemented (effort).
* They are constraints on data, therefore might hide problems. E.g. If I have 100 ‘bad’ inputs, functional dependency is going to keep my database intact and I can carry on without understanding why I have ‘bad’ inputs.

## Anomalies

If a database design contain anomalies, managing a database is next to impossible.

For example, data items might be scattered and not linked together other properly. This means when we try to update one item, with copies scattered over several places, a few instances get updated properly while a few others are left with old values. Such instances leave the database in an inconsistent state.

### Some types of anomalies:

* Deletion anomalies
  - We tried to delete a record, but parts of it was left undeleted because of unawareness, the data is also saved somewhere else.
* Insert / Update anomalies
  - We tried to insert / update data in a record that does not exist.

## Normalization

Normalization is a method to remove all anomalies and bring the database to a consistent state. It is a technique of organizing the data in the database.

Normalization is a systematic approach of decomposing tables to eliminate data redundancy (repeated data) and undesirable characteristics like insertion, update and deletion anomalies.

It is a multi-step process that puts removes duplicated data from the relation tables.

Normalizations are guidelines and guidelines only. Occasionally, it becomes necessary to stray from them to meet practical business requirements. However, when variations take place, it's extremely important to evaluate any possible ramifications they could have on your system and account for possible inconsistencies.

Normalization comes in four/five flavours:
* First Normal Form
* Second Normal Form
* Third Normal Form
* BCNF (aka third and a half form)
* Fourth Normal Form
* Fifth Normal Form (beyond the scope of this course)

These normalization guidelines are cumulative. For a database to be in 2NF, it must first be 1NF.

While database normalization is often a good idea, it's not an absolute requirement. In fact, there are some cases where deliberately violating the rules of normalization is a good practice.

### First normal form (1NF)
Sets the very basic rules for an organized database:
- Eliminate duplicative columns from the same table.
- Create separate tables for each group of related data and identify each row with a primary key.

### Second normal form (2NF)
Further addresses the concept of removing duplicative data:
- Meet all the requirements of the first normal form.
- Remove subsets of data that apply to multiple rows of a table and place them in separate tables.
- Create relationships between these new tables and their predecessors through the use of foreign keys.

### Third normal form (3NF)
Goes one large step further:
- Meet all the requirements of the second normal form.
- Remove columns that are not dependent upon the primary key.

### The Boyce-Codd Normal Form,
Also referred to as the "third and half (3.5) normal form", adds one more requirement:
- Meet all the requirements of the third normal form.
- Every determinant must be a candidate key.

### Fourth normal form (4NF)
Has one additional requirement:
- Meet all the requirements of the third normal form.
- A relation is in 4NF if it has no multi-valued dependencies.

## Resources:

* [Functional dependency - Edu grabs](http://www.edugrabs.com/functional-dependency/)
* [Database normalization - Study tonigth](http://www.studytonight.com/dbms/database-normalization.php)
* [Database Normalization Basics - Though Co](https://www.thoughtco.com/g00/database-normalization-basics-1019735)
