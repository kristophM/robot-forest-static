---
title: "Python Loops"
date: 2019-06-26T22:20:08-04:00
draft: false
sort_key: 14.5
category: "Python"
---
# Python Loops
Executing code based on conditions is very easy with Python, and like other
languages, except with indentation and a few idioms.

# While Loops

While loops behave similarly to those in other programming languages.

```python
x = 10
while x > 0:
  print(x)
  x -= 1
```

## Break and Continue

The `break` keyword allows one to break out of the current loop. This works in other
Python loops as well.

```python
x = 10
while x > 0:
  if x == 5:
    print("reached 5. Exiting...")
    break
  print(x)
  x -= 1
print('Completed.')
```

The `continue` keyword will interrupt the existing iteration in the loop and move on
to the next one.

```python
x = 10
while x > 0:
  if x == 5:
    print("skipping 5...")
    x -= 1
    continue
  print(x)
  x -= 1
print('Completed.')
```

# For Loops

For loops behave similarly as for loops in other languages. There are two main ways
to iterate using for loops: by value of a collection, or by index.

```python
x = [4, 5, 6]

# Iterate by value:
for e in x:
  print(e)

# Iterate by index
for i in range(0, len(x)):
  print("value", x[i], "at index", i)
```

## Break and Continue

The `break` and `continue` keywords behave exactly the same as above for _while loops_
as they do for _for loops_.

## Nesting Loops

For loops may be nested within each other by successive indentations.

```python
x = [
  [1, 4, 7],
  [4, 9, 0],
  [3, 2, 5]
]
sum = 0
for m in range(0, len(x)):
  for n in range(0, len(x[m])):
    sum += x[m][n]
print(sum)
```

## Else

In Python _for loops_, the `else` keyword allows you to run code at the end of the loop.

```python
x = [4, 5, 6]

for e in x:
  print(e)
else:
  print("Done!")
```
