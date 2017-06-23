# Data Models

## Table of Contents

* [Introduction](#introduction)
* [Entity Relationship models](#entity-relationship-models)
* [Relational models](#relational-models)
* [Transforming ER models to relational models]((#transforming-er-models-to-relational-models))
* [Resources](#resources)

## Introduction

Data models represent a database as a diagram. They can be used to design databases, or visualise the structure of an existing database.

In this chapter we will look at two data models

1. Entity-Relationship models (Mind maps)
2. Relational models (Database tables with fields and datatypes)

## Entity Relationship models

Entity Relationship (ER) data models are often based on real-world entities and the relationships among them. They are used to design a database. ER models are mind maps.

ER Data Model include:

1. Entities and their attributes
  * E.g. a person is an entity, that person's name and phone number are attributes.
  * Entities may eventually become DB tables.
  * Entities are represented by rectangles (see "Person" in the diagram below)
  * Attributes will eventually become DB fields
  * Attributes are represented by ovals (see "Name" in diagram below).
2. Relationships among entities
  * Relationships are represented by a diamond and described by a verb (e.g. have, own, buy, etc...)
  * Sometimes, a numbers or symbols to represent type of relationship (e.g. one-to-one, one-to-many, etc...)

![Example ER model](http://www.learndb.com/wp-content/uploads/2014/03/convert-ER-Diagram-Relation-Schema3.png)
> From [Learn Databases](http://www.learndb.com/databases/how-to-convert-er-diagram-to-relational-database) by [Imed Bouchrika](https://plus.google.com/+ImedBouchrikaWeb)


### Types of Attributes

Attributes can be described in the following way:

*  Simple attribute:
  - These are *atomic* values (they cannot be divided further).
  - For example, a student's phone number is an atomic value of 10 digits.
  - Represented in ER diagram by a single oval (as in diagrams above)
* Composite attribute:
  - Made of more than one simple attribute.
  - For example, a student's complete name be made of their first_name and last_name.
* Derived attribute:
  - Attributes will not exist in the database, as their values can be derived from other attributes present in the database.
  - For another example, age can be derived from data_of_birth.
  - Represented in ER diagram with a dashed line (see "Age" in diagram below)
* Single-value attribute:
  - Can only appear once for each entity.
  - For example, Social_Security_Number.
  - Represented in ER diagram by a single oval (as in diagrams above)
* Multi-value attribute
  - Contain more than one values.
  - For example, a person can have more than one phone number, email_address, etc.
  - Represented in ER diagram by a double oval (see "Phone" below)

### Mapping Cardinalities

Cardinality defines the number of entities in one entity set, which can be related to a number of entities in other set.

For example, a woman can only have one husband (in monogamous societies), but she might have several children. A company might have many workers, who might each work at many companies.

* One-to-one
  - One entity from entity set A can be associated with at most one entity of entity set B and vice versa.
  - Wife to husband
* One-to-many
  - One entity from entity set A can be associated with more than one entities of entity set B however an entity from entity set B, can be associated with at most one entity.
  - Mother to children
* Many-to-one
  -  More than one entities from entity set A can be associated with at most one entity of entity set B, however an entity from entity set B can be associated with more than one entity from entity set A.
  - Children to father
* Many-to-many
  - One entity from A can be associated with more than one entity from B and vice versa.
  - Brothers to sisters

These values are represented by "1" and "M" in the ER model (see below)

### Complete ER model example
![ER models with attribute types and Cardinality](http://www.learndb.com/wp-content/uploads/2014/03/convert-ER-Diagram-Relation-Schema.png)

> From [Learn Databases](http://www.learndb.com/databases/how-to-convert-er-diagram-to-relational-database) by [Imed Bouchrika](https://plus.google.com/+ImedBouchrikaWeb)

## Relational models

A Relational model is a more formal description of the structure of a database. It includes, table names, fields, and relations. It should also include datatypes (INT, VARCHAR, etc...). Primary and foreign keys should
be clearly labelled (e.g. "PK", "FK"). These relations between tables are sometimes identified with lines which show cardinality (one-to-one, one-to-many, etc...).

*Note: Ignore the Indexes in the diagram below. Indexing is beyond the scope of this course.*

![Example relational model](https://upload.wikimedia.org/wikipedia/commons/5/50/Relational.png)
> [Example Relational model by Tsedenjav.Sk/Wikipedia](https://commons.wikimedia.org/wiki/File:Relational.png) is licensed under CC BY-SA 4.0

## Transforming ER models to relational models

Relational models are often derived from ER models by following these steps:

- Create tables for all entities.
- Include a primary key in each table
- Add attributes as fields in the table
- Include primary keys as foreign key attributes in related entities.

## Resources:

* [Tutorial point - ER diagram representation](https://www.tutorialspoint.com/dbms/er_diagram_representation.htm)
* [Learn Databases - how to convert ER to Relational Modela](http://www.learndb.com/databases/how-to-convert-er-diagram-to-relational-database)
* [Tutorial point - ER model to relational mode](https://www.tutorialspoint.com/dbms/er_model_to_relational_model.htm)
