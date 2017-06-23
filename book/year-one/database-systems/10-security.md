# Chapter 02

## Table of Contents

* [Chapter heading](#chapter-heading)
* [Resources](#resources)

## Introduction



## Security risks

* Excessive, Unused Privileges and/or Privilege Abuse
  - Database users may have too much power to access and change a database.
  - For instance a non-technical colleague with admin rights over a database migth accidentally delete everything.
* Input Injections
  - SQL queries coming from insecure locations (e.g. members of the public submitting SQL queries in a web form)
* Malware
  - Viruses and other nasties
* Weak Audit Trail
  - Undocumented access (access logs) to the database may make it impossible to identify the source of changes / problems.
* Storage Media Exposure
  - Unsecured backups.
* Exploitation of Vulnerable, Misconfigured Databases
  - Hacking.
* Unmanaged Sensitive Data
  - Unrestricted access to private user data (e.g. Health records)
* Denial of Service
  - Bots generating huge amounts of traffic to bring down a server
* Limited Security Expertise and Education
  - Lack of understanding about these risks is a risk in itself

## Password hashing

A hash is designed to act as a "one-way function": A mathematical operation that's easy to perform, but very difficult to reverse. Like other forms of encryption, it turns readable data into a scrambled cipher. But instead of allowing someone to decrypt that data with a specific key, as typical encryption functions do, hashes aren't designed to be decrypted. Instead, when you enter your password on a website, it simply performs the same hash again and checks the results against the hash it created of your password when you chose it, verifying the password's validity without having to store the sensitive password itself.

https://www.wired.com/2016/06/hacker-lexicon-password-hashing/

## Encryption
Encryption is a security method in which information is encoded in such a way that only authorized user can read it. It uses encryption algorithm to generate ciphertext that can only be read if decrypted.

https://www.tutorialspoint.com/internet_technologies/data_encryption.htm

## SQL Injection
If you take a user input through a web page and insert it into a SQL database, there is a chance that you have left yourself wide open for a security issue known as the SQL Injection.

Injection usually occurs when you ask a user for input, like their name and instead of a name they give you a SQL statement that you will unknowingly run on your database. Never trust user provided data, process this data only after validation; as a rule, this is done by Pattern Matching.

https://www.tutorialspoint.com/sql/sql-injection.htm


## Resources:

* [Link text](http://www.example.co.uk/)
