---
title: "Functions"
date: 2019-06-23T22:20:25-04:00
draft: true
sort_key: 15
category: "Python"
---

# Python Functions

Python functions are very straightforward and follow the same pattern of indentation
that you would expect.

## Defining a function and Calling it

Functions are defined by the `def` keyword, followed by a name and parentheses
containing arguments, and then a colon (":"). The body of the function MUST be indented.

Calling a function is as simple as using its name, followed by parentheses.

```python
def greet():
  print("Bonjour!")

greet()
```

Unlike in Ruby, you MUST specify parentheses even if your function doesn't take
arguments.

### Specifying arguments
Parameters are specified within the parentheses, separated by commas.

```python
def greet(language, night_or_day):
  if language == 'English':
    if night_or_day == 'day':
      print('Hello')
    else:
      print('Good Night')
  elif language == 'French':
    if night_or_day == 'day':
      print('Bonjour')
    else:
      print('Bonsoir')

greet('French', 'day')
greet(night_or_day='day', language='French') # Equivalent
```

Note that when calling a function, Order matters unless using named parameters using the "=" (equals) symbol.

### Setting default values for arguments

Default arguments can be specified using an equals sign.

```python
def add(x, y=7):
  return x + y

add(2) # return 9
```

## Returning values

To return values, you MUST use the `return` keyword (unlike in Ruby, for example).

```python
def switch(x, y=7):
  return (y, x)

a, b = switch(7,5)
print(a, b)
```

Note that for functions that return a tuple, you can "deconstruct" the returned tuple
into separate variables and assign them directly. In the above example, "a" and "b"
get assigned automatically to the components of the returned tuple. 
