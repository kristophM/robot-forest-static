---
title: "Tuples"
date: 2019-06-23T22:05:20-04:00
draft: false
sort_key: 10
category: "Python"
---

## Python Tuples

A tuple is a collection which is *ordered* and *unchangeable*. In Python, tuples
can contain multiple types. Tuples are often most useful when you need an object
that holds multiple values, but don't want to invest in the heavy effort of creating a whole
class.


## Create a Tuple

```python
tup = ('Illustrator', 20.99, 'Pro')
print(tup)
```

NOTE: Tuples cannot be changed once created.

## Accessing Tuple Values

You can access tuple items by their index using brackets ("[]").

```python
tup = ('Illustrator', 20.99, 'Pro')
print(tup[1])
```

## Iterate Through Tuple Values

Iterating through tuples is easy with for loops.

```python
tup = ('Illustrator', 20.99, 'Pro')
for e in tup:
  print(e)
```

## Add and Remove Tuple Items

Tuples are unchangeable so you may not add or delete items. You can however remove
the entire tuple from memory.

```python
tup = ('Illustrator', 20.99, 'Pro')
# Delete entire tuple
del tup
print(tup) # Will result in an error
```
