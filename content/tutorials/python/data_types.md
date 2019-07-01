---
title: "Data Types"
date: 2019-06-23T22:04:14-04:00
draft: true
sort_key: 5
category: "Python"
---
# Python Data Types

Python has very few primitive types: int, float, string, and boolean

## Python Numeric Types

Python has three types of numbers in its core library:

* int

* float

* complex

### Int

Integers are whole numbers, positive or negative, with unlimited length. It's not
necessary to specify the precision bits (8, 16, 32, 64) like in other languages,
as Python handles memory management automatically and there is not a set limit in
bits that an integer can be.

```python
x = 5
y = 239847239847234 # Really big numbers are ok!
z = -9823498237498
```

### Float

Floating point numbers are numbers, positive and negative that contain at least
one decimal place. Again, specifying the precision is not necessary in Python.

```python
x = 234.8
y = 1.
z = 1.0
m = 3e3
n = -3.4
```

Note the usage of scientific notation, and dots without trailing numbers!

### Complex

Complex (a.k.a. "imaginary") numbers are written with a "j" to specify their
imaginary component.

```python
x = 4 + 2.3j
y = 50j
```

## Python String Variables

String variables can be defined either using single or double quotes.

```python
x = "Hello"
y = 'Hello'
print(x == y) # => True
```

Why are there both single and double quotes then? You may want to have literal
quotes inside of a string, without needing to escape the quotes. For example:

```python
greeting = 'Hello, "Shanna"'
print(greeting)
```

Note how the double quotes are preserved in the string.

## Python Boolean

Python booleans behave similarly to in other languages, but note the capitalized
letters in `True` and `False`

```python
x = True
y = 5 > 5 # => False
z = False
```

# Null
To represent a null value in Python, use the `None` keyword.

```python
x = None
```
