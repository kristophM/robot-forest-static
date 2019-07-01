---
title: "Variables"
date: 2019-06-23T22:04:02-04:00
draft: false
category: "Python"
sort_key: 4
category: "Python"
---

# Python Variables

Python variables are created as soon as you define them and don't need to be
initialized, nor do their types need to be specified.

```python
num_apples = 5 # initialized automatically as type "int"
greeting = 'Hallo' # initialized automatically as type string?
avg = 6.4 # initialized automatically as type float?
print(num_apples, greeting, avg)
```

### Tip: Determine the type of a variable

Use `type()` to determine the type (or class) of a variable.

```python
x = 5
y = "Hallo"
z = 2e6

print(type(x))
print(type(y))
print(type(z))
```

## Variable Name Rules

Variables in Python have the following rules:

* They must start with a letter

* They must contain only alphanumeric characters and underscores

* They are case sensitive
