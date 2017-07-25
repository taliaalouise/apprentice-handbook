# ACID

## Table of Contents

* [Introduction](#introduction)
* [Atomicity](#atomicity)
* [Consistency](#consistency)
* [Durability](#durability)
* [Isolation](#isolation)
* [Resources](#resources)

## Introduction

A transactions in a database system must maintain Atomicity, Consistency, Isolation, and Durability − commonly known as ACID properties − in order to ensure accuracy, completeness, and data integrity.

## Atomicity

Atomicity states that a transaction are 'all or none'. That is, either all operations are executed or no operations are executed. There must be no state in a database where a transaction is left partially completed. If a steps fails or is aborted, the DBMS should roll back all changes to the point before the transaction began

## Consistency

The database must remain in a consistent state after any transaction. No transaction should have any adverse effect on the data residing in the database. If the database was in a consistent state before the execution of a transaction, it must remain consistent after the execution of the transaction as well.

## Durability

The database should be durable enough to hold all its latest updates even if the system fails or restarts. If a transaction updates a chunk of data in a database and commits, then the database will hold the modified data. If a transaction commits but the system fails before the data could be written on to the disk, then that data will be updated once the system springs back into action.

## Isolation

In a database system where more than one transaction are being executed simultaneously and in parallel, the property of isolation states that all the transactions will be carried out and executed as if it is the only transaction in the system. No transaction will affect the existence of any other transaction.

## Resources:

* [Tutorials Point - DBMS Transactions](https://www.tutorialspoint.com/dbms/dbms_transaction.htm)
