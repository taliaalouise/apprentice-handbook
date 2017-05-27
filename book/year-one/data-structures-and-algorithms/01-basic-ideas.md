# Basic Ideas and Skills

## Table of Contents

* [What is an algorithm](#what-is-an-algorithm)
* [Pseudocode](#pseudocode)
* [Resources](#resources)

## What is an algorithm?

An algorithm is a list of steps or a series of instructions. We use algorithms all the time and not just in computers. Cooking recipes and guides to building flat-pack furniture are algorithms. Programs are algorithms written for a computer in a programming language.

Formal definition:
> a process or set of rules to be followed in calculations or other problem-solving operations, especially by a computer.

## Pseudocode

Developers sometimes use pseudocode to plan and visualise a program before they begin writing it in a programming language. It can help develop efficient code and identify bugs. 

Experienced developers may never actually write pseudocode, but will go through the process of structuring and planning an algorithm in their head.

### How to write pseudocode

Like programming languages, pseudocode has syntax (or conventions). Different people use different conventions, just like they use different programming langauges. These are the conventions used at ADA College.

#### Assigning a value to a variable

Use the arrow symbol ← for assignemnt: `varibleName ←  value`

e.g. `score ←  10`

#### Equality

The equals sign (=) represents strict equality (equivalent to "==" in Java)

e.g. `if score = 0 then`

#### Input

`input` means an input to the program (maybe from a user).

e.g. `input username`

#### Output

`print` denotes show output to user.

e.g. `print “this string”`

#### Conditionals

```
if marks > 50 then 
	print “Congratulation, you have passed!”
else if marks < 0 then
	print “Cannot be less than 0”
else
	print “Sorry, you are failed!”
end if
```

#### While loops

```
counter ← 0
while counter < 5 do 
	print “Welcome to ADA!”
	counter ← counter + 1
end while
```

#### For loops

```
for counter ← 0; counter < 5; counter ← counter + 2 do 
	print “Welcome to ADA!”
end for
```

#### Arrays
`A[n]` represents the *nth* item in the array A. 

The cells of an n-celled array A are indexed from `A[0]` to `A[n − 1]` (consistent with Java).

#### Comments

```
/* Multiple line comments
go here. */
``` 

`// Single line comments go here`

Some people prefer braces `{for comments}`

## Resources:

* [BBC: What is an algorithm? (video)](http://www.bbc.co.uk/guides/z3whpv4).
* [BBC: What is an algorithm? (infographic)](http://www.bbc.co.uk/guides/zqrq7ty)
* [BBC: Pseudocode](http://www.bbc.co.uk/education/guides/z3bq7ty/revision/2)
* [Khan Academy: Planning with pseudocode](https://www.khanacademy.org/computing/computer-programming/programming/good-practices/p/planning-with-pseudo-code)
