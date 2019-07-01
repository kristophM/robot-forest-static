---
title: "Lambdas"
date: 2019-06-23T22:20:25-04:00
draft: false
sort_key: 15
category: "Python"
---

# Python Lambdas

Lambdas are small anonymous functions. They are often used to pass functions as
arguments into other functions, and can accept any number of arguments, but MUST
have only ONE expression.

## Syntax

The lambda syntax in Python involves using the `lambda` keyword, along with some
argument names, followed by a colon (":"), and an expression to be returned.

```
lambda arguments : expression
```

NOTE: In lambdas, `return` keywords are not used in the expression, since a lambda
only allows one expression, the content of which is returned.

```python
selector = lambda e : e > 0 # return true if element is greater than zero
s = [4, 5, -6]
result = map(selector, s)
print(list(result))
```

## When to Use Lambdas

When to use lambdas vs. regular functions in Python? Usually a good time to use
lambdas is when you need to pass a function as an argument into another function.
For example, the `map()` function above takes in a function as an argument. Writing
an anonymous function is a much more compact way to describe a functionality than
to write a regular named function. See how compact we can make the above logic:

```python
s = [4, 5, -6]
result = map(lambda e : e > 0, s)
print(list(result))
```
