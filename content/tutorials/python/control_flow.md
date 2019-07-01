---
title: "Control Flow"
date: 2019-06-23T22:20:08-04:00
draft: false
sort_key: 14
category: "Python"
---
# Python Control Flow
Executing code based on conditions is very easy with Python, and like other
languages, except with indentation and a few idioms.

## If... Else

```python
x = 5
if x < 7:
  print("success")
else:
  print("nope")
```

## Elif

```python
x = 7
if x < 7:
  print("success")
elif x == 7:
  print("exact match")
else:
  print("nope")
```

## Python's answer to the Ternary Operator

In other languages such as Ruby and Javascript you may be used to seeing a so-called
"ternary" operator of the form `x == 5 ? doSomething() : doTheOtherThing()`,
allowing you to specify an if...else statement *inline*. Python can do the same,
but it takes a different form. See the example below:

```python
print("limit not yet reached") if x < y else print("too much")
```

## Shorthand If

Similarly, if you don't need to specify an "else" condition, there's a shorthand
`if` in Python

```python
if x < y: print("limit not yet reached!")
```

## And and Or
Python has the following binary operators that are similar to `&&` and `||` in
other languages: `and` and `or`.

```python
if x < y and a > b:
  print("good")
```

```python
if x < y or a > b:
  print("also good")
```

# Python Switch - Case Statements

Python, unlike most languages, does not have `switch` statements built in. Rather,
it favors if..else statements as illustrated above.
