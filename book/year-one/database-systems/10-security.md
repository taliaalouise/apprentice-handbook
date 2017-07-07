# Security

## Table of Contents

* [Introduction](#Introduction)
* [Security risks](#security-risks)
* [Password hashing](#password-hashing)
* [Encryption](#Encryption)
* [SQL Injection](#sql-injection)
* [Resources](#resources)

## Introduction

This chapter contains an non-exhuastive list of security risks and then goes into detail on some security issues that are key to database management.

## Security risks

* Incorect user privileges
  - Database users may have too much power to access and change a database.
  - For instance a non-technical colleague with admin rights over a database migth accidentally delete everything.
* SQL injections
  - SQL queries coming from insecure locations (e.g. members of the public entering raw SQL queries in a web form intended for data input)
* Malware
  - Viruses and other nasties
* Weak audit trail
  - Undocumented access (access logs) to the database may make it impossible to identify the source of changes / problems.
* Unsecured backups
  - Aka 'storage media exposure'.
  - Your production database is super secure, but your backups are on a insecure server.
* Hacking
  - Exploitation of vulnerable or misconfigured databases.
* Unmanaged sensitive data
  - Unrestricted access to private user data (e.g. Health records).
* Denial of service
  - Bots generating huge amounts of traffic to bring down a server.
* Limited security expertise and education
  - Lack of understanding about these risks is a risk in itself.

## Password hashing

A hash, like other forms of encryption, turns readable data into a scrambled cipher. But instead of allowing someone to decrypt that data with a specific key, as typical encryption functions do, hashes are not designed to be decrypted. Instead, when you enter your password on a website, it simply performs the same hashing algorithm again and checks the results against the hash it stored when you chose your password. This way, the password is verified without having to store the sensitive password itself.

For example, the string `"password"` would be hashed to `"5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8"` using the SHA-1 algorithm. **WARNING:** [SHA-1 is no longer considered secure](https://en.wikipedia.org/wiki/SHA-1).

If someone hacks into a database, they only can access the hashed password data. This does not allow them to access the account as there is no way of getting from the hashed data back to the password.

However, hackers do look for hashes of common passwords (they might search the database for the hash of "password" shown above) as this will allow them identify a password and access a user account. Hence, it is very important to use complex passwords; hackers are unlikely to search for these hashes.

## Encryption

Encryption is a security method in which information is encoded in such a way that only authorized user can read it. It uses encryption algorithm to generate ciphertext that can only be read if decrypted.

## SQL Injection

If you take a user input (e.g. through a form on a web page) and insert it into a SQL database, there is a chance that you have left yourself wide open for a security issue known as the SQL Injection.

Injection usually occurs when you ask a user for input, like their name, and instead of a name they give you a SQL statement that you will unknowingly run on your database. Never trust user provided data, process this data only after validation; as a rule, this is done by Pattern Matching (finding potential dangerous characters and removing them from the data).

![Little Bobby Tables](https://imgs.xkcd.com/comics/exploits_of_a_mom.png)
> ["Exploits of a mum"](https://xkcd.com/327/) by xkcd is licensed under CC BY-NC 2.5

## Resources:

* [Hacker Lexicon: What is password hasing? - Wired](https://www.wired.com/2016/06/hacker-lexicon-password-hashing/)
* [Data encryptoin - Tutorials Point](https://www.tutorialspoint.com/internet_technologies/data_encryption.htm)
* [SQL Injection - Tutorials Point](https://www.tutorialspoint.com/sql/sql-injection.htm)
