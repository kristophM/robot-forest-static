---
title: "Printing and Comments"
date: 2019-06-23T22:02:57-04:00
draft: true
sort_key: 2
category: "Python"
---

# Printing Strings

Print statements use the `print()` command. In Python 3 and later, `print`
must accept arguments in parentheses.

You may put as many arguments as you'd like, separated by commas.

```python
print('Hey')
print('Hello', 'Hallo', 'Hola')
```

## Printing Interpolated Strings

To insert content directly into strings, you can use the `format` method and utilize
brackets as placeholders.

```python
str = "The {} train is running with delays."
print(str.format(7))

# You can have multiple placeholders in a string.
str = "The {} train is running with delays. Use the {} train instead"
print(str.format('6', '4 or 5'))

# Placeholders can also be named.
str = "The {train} train is running with delays. The delay is {delay_time} minutes."
print(str.format(delay_time=10, train='A'))
# Note that named placeholders don't need to be called in order.
```

# Creating Comments

Comments in Python are created by beginning your text with a "#" character. You
may start the line with a "#" or start a comment at the end of the line.

```python
# This is a comment.
```
