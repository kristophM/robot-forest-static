---
title: "Strings"
date: 2019-06-23T22:04:38-04:00
draft: true
sort_key: 6
category: "Python"
---
# Python strings

In Python, like in other classic programming languages, strings are simply arrays
of characters. More specifically, they are arrays of bytes representing unicode
characters.

## Declaring Strings

Strings can be declared with either single or double quotes. By having two types,
you may include quotes in your strings without needing to escape them.

```python
my_string = 'Wild thing, you make my heart sing.'
my_string2 = '"Wild thing", you make my heart sing.'

print(my_string)
print(my_string2)
```

## Multiple Lines

Strings can span multiple lines using triple quotations ('"""')

```python
shakespeare_txt = """
This foul Egyptian hath betrayed me:
My fleet hath yielded to the foe, and yonder
They cast their caps up and carouse together
Like friends long lost. Triple-turned whore! 'tis thou
Has sold me to this novice, and my heart
"""
print(shakespeare_txt)
```

## Interpolating Strings

You may want to assign values to existing strings to format them with custom data.
Python makes this easy with braces.

```python
str = "Your order has been completed and we will send {} flowers."
print(str.format(5))
```

### Index Numbers

For cases where multiple values need to be inserted into a string, you may use indices.

```python
str = "Hi {0}, Your order has been completed and we will send {1} flowers."
print(str.format('Mark', 5))
```

### Named Indices

Or you can use named arguments to further clean up the string formatting!

```python
str = "Hi {name}, Your order has been completed and we will send {qty} flowers."
# Notice that the arguments are allowed to be out of order since they are named!
print(str.format(qty=5, name='Mark'))
```

## Useful String Methods

Here are some useful string methods to memorize.

```python
# len()
str = "The quick brown fox jumped over the lazy dog's back.    " # Whitespace intentional
print(len(str))

# character at a position
print(str[0])

# trim whitespace using strip()
print(str.strip())

# split into list
print(str.split())

# replace words with string 
print(str.replace('fox', 'bear'))

# lower/upper case
print(str.upper())

```
