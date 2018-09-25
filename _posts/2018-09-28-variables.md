---
layout:     post
title:      Variables
date:       2018-09-28
summary:    Using Variables
categories: cst
---

## What Are Variables
Variables are the most basic part of data storage and organization, and their function is simple: hold values that can vary. In Processing, and most languages, variables have types.
This means that different values have to be stored in different types of variables. These types are known as **primitives**. Since Processing uses Java as a backbone,
the primitives are the same for both languages.
#### Primitives
* `int`
* `float`
* `double`
* `long`
* `char`
* `byte`
* `boolean`
* `color` (only in Processing)

We will learn what values correspond to what primitives, but for now, we will mostly use `int`, `double`, `char`, `boolean`, and `color`.

## A Lesson in Binary
For many, binary is just 1s and 0s jumbled together as nonsense, but to computers, binary is their language. Electrical flow can be though of as either on or off, and these states are encoded as 1s and 0s in binary.
The simplest unit of memory in a computer is the byte: a collection of 8 bits, where a bit is the flow state (1 or 0). All values that we use can be encoded as binary, and converting them depends on the value type.

#### Understanding Binary Notation
The number 678 can be thought of as 8 ones, 7 tens, and 6 hundreds. This because decimal numbers use base-10, or powers of 10 to express numbers. So 678 can be written as (8 * 10^0) + (7 * 10^1) + (6 * 10^2).

Binary is base-2, so numbers are written as a sum of powers of 2. Take the number 13. 13 can be thought of as 1 one, 1 four, and 1 eight, or (1 * 2^0) + (1 * 2^2) + (1 * 2^3).

If you look at the exponents used, you can 
organize the sum like this: 1101. From right to left, there are values at positions 1, 3, and 4, or exponents 0, 2, and 3. In general, binary can be thought of as a series of powers of two that are 'active' or 'inactive', and 
adding up the 'active' powers will get us the decimal (base-10) equivilent. 

#### Converting Decimals to Binary
The general method to convert decimal to binary is to find the greatest power of two that is less than or equal to the number, subtract it, and repeat, marking down which powers work. 
For example, the number 89 fits 64, or 2^6, and 89 - 64 is 25. 25 fits 16, or 2^4, and 25 - 16 is 9. 9 fits 8, or 2^3, and 9 - 8 is 1. Finally 1 fits 1, or 2^0, and 1 - 1 is 0. 
Looking at the powers, we have 6, 4, 3, and 0, so, from right to left, we know positions 1, 4, 5, and 7 are active. In binary notation: 1011001.