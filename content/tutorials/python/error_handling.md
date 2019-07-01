---
title: "Error Handling"
date: 2019-06-23T22:35:56-04:00
draft: true
sort_key: 22
category: "Python"
---

# Python Error Handling

Python handles exceptions in a similar manner to other languages using `try`,
`except`, and `finally`.

The `try` block allows you to write code that has the potential of raising an exception.

The `except` block intercepts the exception before a crash is about to occur, and
lets you handle the exception.

The `finally` block executes no matter what, at the end of the try-except block.

## Handle the Exception

If you suspect a block of code has a chance of failing, wrap the code in a _try...except_
block.

```python
try:
  5/0
except:
  print("an error occurred")
```

If you can further anticipate certain types of exceptions and wish to handle them
in a specialized manner vs other exceptions, you can name them explicitly:

```python
try:
  5/0
except ZeroDivisionError:
  print("you cannot divide by zero!")
```

## Handle Multiple Exceptions

If you anticipate *multiple* types of errors ocurring, you can handle them all
separately:

```python
try:
  c = a / b
except ZeroDivisionError:
  print("you cannot divide by zero")
except NameError:
  print("are you sure you've defined your variables?")
```

## Else

You can also specify a block of code to execute ONLY if there were no errors.

```python
try:
  c = 5 // 2
except ZeroDivisionError:
  print("you cannot divide by zero")
else:
  print("everything good")
```

## Finally

You can add `finally` to ensure that certain code executes regardless of success
or failure.

```python
try:
  c = 5 // 0
except ZeroDivisionError:
  print("you cannot divide by zero")
finally:
  print("ok let's get on with it!")
```
