---
title: "Operators"
date: 2019-06-23T22:04:58-04:00
draft: false
sort_key: 8
category: "Python"
---

# Python Operators

Python has all the standard operators for working with data and logic, however,
many of the language's unique idioms reveal themselves here.

## Arithmetic Operators

Arithmetic operators are for basic math operations on numerical variables. Note that
some operations, such as the plus sign ("+") can be applied to strings and lists,
and not just numerical variables.

| Operator | Name           | Example |
|----------|----------------|---------|
| +        | Addition       | x + y   |
| -        | Subtraction    | x - y   |
| *        | Multiplication | x * y   |
| /        | Division       | x / y   |
| %        | Modulus        | x % y   |
| **       | Exponentiation | x ** y  |
| //       | Floor division | x // y  |

TODO: [REPL]

## Assignment Operators

Assignment operators are for assigning values to variables

| Operator | Example | Same As    |
|----------|---------|------------|
| =        | x = 5   | x = 5      |
| +=       | x += 3  | x = x + 3  |
| -=       | x -= 3  | x = x - 3  |
| *=       | x *= 3  | x = x * 3  |
| /=       | x /= 3  | x = x / 3  |
| %=       | x %= 3  | x = x % 3  |
| //=      | x //= 3 | x = x // 3 |
| **=      | x **= 3 | x = x ** 3 |
| &=       | x &= 3  | x = x & 3  |
| |=       | x |= 3  | x = x | 3  |
| ^=       | x ^= 3  | x = x ^ 3  |
| >>=      | x >>= 3 | x = x >> 3 |

[REPL]

## Comparison Operators

Comparison operators compare two variables and return a boolean.

| Operator | Name                     | Example |
|----------|--------------------------|---------|
| ==       | Equal                    | x == y  |
| !=       | Not equal                | x != y  |
| >        | Greater than             | x > y   |
| <        | Less than                | x < y   |
| >=       | Greater than or equal to | x >= y  |
| <=       | Less than or equal to    | x <= y  |

[REPL]

## Logical Operators

Logical operators combine conditional statements.

| Operator | Description                                             | Example               |
|----------|---------------------------------------------------------|-----------------------|
| and      | Returns True if both statements are true                | x < 5 and  x < 10     |
| or       | Returns True if one of the statements is true           | x < 5 or x < 4        |
| not      | Reverse the result, returns False if the result is true | not(x < 5 and x < 10) |

[REPL]

## Identity Operators

Identity operators are used to check if an object is in fact identical to another based on
memory location.

| Operator | Description                                            | Example    |
|----------|--------------------------------------------------------|------------|
| is       | Returns true if both variables are the same object     | x is y     |
| is not   | Returns true if both variables are not the same object | x is not y |

[REPL]

## Membership Operators

Membership operators test to see if something is contained within an object/collection.

| Operator | Description                                                                      | Example    |
|----------|----------------------------------------------------------------------------------|------------|
| in       | Returns True if a sequence with the specified value is present in the object     | x in y     |
| not in   | Returns True if a sequence with the specified value is not present in the object | x not in y |

[REPL]

## Bitwise Operators  

Bitwise operators compare binary numbers.

| Operator | Name                 | Description                                                                                             |
|----------|----------------------|---------------------------------------------------------------------------------------------------------|
| &        | AND                  | Sets each bit to 1 if both bits are 1                                                                   |
| |        | OR                   | Sets each bit to 1 if one of two bits is 1                                                              |
| ^        | XOR                  | Sets each bit to 1 if only one of two bits is 1                                                         |
| ~        | NOT                  | Inverts all the bits                                                                                    |
| <<       | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off                        |
| >>       | Signed right shift   | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |

[REPL]
