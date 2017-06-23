# Chapter 02

## Table of Contents

* [Introduction](#introduction)
* [Text types](#text-types)
* [Number types](#number-types)
* [Date types](#date-types)
* [Boolean types](#boolean-types)
* [Resources](#resources)

## Introduction

Datatypes are used to tell the database what kind of data should go into specific fields in a database. This is important as it ensures databases function properly.
* It minimises human error: If someone accidental tries to put a name in a date field, the database will raise an error.
* It ensures all data in the field can be compared / analysed properly. For instance, if an age field that only accepts integers we eliminate the possibilty of 7 + "seven" (which would also raise an error).

Different SQL databases (MySQL, PostgreSQL, Oracle, etc...) handle datatypes slightly differently. In this chapter we will focus on MySQL data tyoes.

## Text types

* `CHAR(n)` A field that stores text of a fixed length of *n* character. *n* can be any value from 0 to 255. If you store a string with <*n* characters, MySQL adds spaces to fill up the empty characters. These spaces are removed by default when a `CHAR` is retrieved from the database
* `VARCHAR(n)`A field that stores a variable length of characters up *n*. *n* can be any value from 0 to 65,535.

## Number types

* `INTEGER`(can also be referred to as `INT`). No decimals. Can store values from -2147483648 to 2147483647
* `FLOAT`	Decimal. Approximate.

## Date types

* `DATE` Stores year, month, and day values
* `TIMESTAMP` Stores year, month, day, hour, minute, and second values

## BOOLEAN types

* `BOOLEAN`	Stores TRUE or FALSE values. (These types are synonyms for TINYINT(1). A value of zero is considered false. Nonzero values are considered true.)

## Resources:

* [MySQL: The CHAR and VARCHAR Types](https://dev.mysql.com/doc/refman/5.7/en/char.html)
* [MySQL: Integer Types](https://dev.mysql.com/doc/refman/5.7/en/integer-types.html)
* [MySQL: Floating-Point Types (Approximate Value)](https://dev.mysql.com/doc/refman/5.7/en/floating-point-types.html)
* [MySQL: The DATE, DATETIME, and TIMESTAMP Types](https://dev.mysql.com/doc/refman/5.7/en/datetime.html)
