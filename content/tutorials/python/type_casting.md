---
title: "Type Casting"
date: 2019-06-23T22:04:22-04:00
draft: false
sort_key: 7
category: "Python"
---

# Python Casting

Casting in Python is typically performed by using constructor functions. Below
you see how numerical types get converted into strings and vice versa.

```python
w = str(8)
x = int(3.8)
y = int("4")
z = float("4")
print(x, y, z)
```

## Implicit vs Explicit Type Casting

*Implicit type casting* happens when an operation you execute in Python forces a
variable to become another type

```python
x = 1 + 2.5
y = "number of apples is: " + 1
print(x, y)
```

*Explicit type casting* happens when you define a cast in the code outright. It takes
the form of `(required_data_type)(expression)`.

```python
# Explicit type casting
float(2)
```
