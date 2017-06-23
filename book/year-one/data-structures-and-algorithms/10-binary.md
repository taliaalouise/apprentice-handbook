# Binary

## Table of Contents

* [Introduction](#introduction)
* [Bit and Bytes](#bits-and-bytes)
* [Binary numbers](#binary-numbers)
* [Two to the power](#two-to-the-power)
* [Memory sizes](#memory-sizes)
* [Resources](#resources)

## Introduction

Computers are machines that process binary data. They work with *0s* and *1s*.

At the very lowest level, computers work with electrical signal. *1* means *on* i.e. a small electrical signal is received, and *0* means *off* i.e. no electical signal is received.

## Bits and Bytes

### Bits

Each binary digit (each *1* or *0*)  is called a bit. For example, these strings are all made up of 4 bits:

| some 4 bit strings |
|---------------|
| 1111          |
| 0000          |
| 1001          |
| 1101          |

### Bytes

A series of 8 bits is called a byte. For example:

| some bytes (8 bits) |
|---------------|
| 11111111          |
| 00000000          |
| 10010101          |
| 11010110          |


## Binary numbers

Computers store numbers as strings of binary digits (e.g. 10101011 will represent a number).

We do not need to know how computers actually encode numbers into binary (in this course). However, we should understand that short bit strings can only store small numbers, and that larger bit strings can hold much larger numbers.

You can calculate the maximum number that can be stored using this formula ![equation](https://latex.codecogs.com/gif.latex?2^{n}-1) (where *n* represents the number of bits). For example, the largest number you can store in a byte (8 bits) is: ![equation](https://latex.codecogs.com/gif.latex?2^{8}-1=255)

### Number types in Java

The fact that longer bit strings can store larger numbers gives rise the different data types in Java. Data types that can store larger numbers use more bits and therefore occupy more memory. This table shows some of the different number data types:

| Data type | Bytes used | Can store decimals |Value range |
|-----------|------------|--------------------|------------|
| int       | 4 bytes    |No                  |-2,147,483,648 to 2,147,483,647|
| long      | 8 bytes    |No                  |-9,223,372,036,854,775,808 to 9,223,372,036,854,775,80|
| float     | 4 bytes    |Yes                 |7 decimal digits|
| double    | 8 bytes    |Yes                 |16 decimal digits|

## Two to the power

Farhad suggested we should know the value for ![equation](https://latex.codecogs.com/gif.latex?2^{n}) while *n <= 10*

|                                                        |  *n* | value |
|--------------------------------------------------------|------|-------|
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  1   | 2     |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  2   | 4     |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  3   | 8     |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  4   | 16    |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  5   | 32    |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  6   | 64    |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  7   | 128   |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  8   | 256   |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  9   | 512   |
|![equation](https://latex.codecogs.com/gif.latex?2^{n}) |  10  | 1024  |

## Memory sizes

Computer memory is measured in bytes. The units of measurement increase, as *n* increases in ![equation](https://latex.codecogs.com/gif.latex?2^{n})

| Memory size | Number of Bytes |
|-------------|-----------------|
| KB          | ![equation](https://latex.codecogs.com/gif.latex?2^{10}) |
| MB          | ![equation](https://latex.codecogs.com/gif.latex?2^{20}) |
| GB          | ![equation](https://latex.codecogs.com/gif.latex?2^{30}) |
| TB          | ![equation](https://latex.codecogs.com/gif.latex?2^{40}) |

## Resources:

* [Binary - BBC Bitesize](http://www.bbc.co.uk/education/guides/z26rcdm/revision)
* [Binary numbers (video)](https://www.youtube.com/watch?v=LpuPe81bc2w)
