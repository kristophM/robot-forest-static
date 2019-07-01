---
title: "Iterators"
date: 2019-06-23T22:20:30-04:00
draft: true
sort_key: 16.8
category: "Python"
---

# Python Iterators

An *iterator* in Python is an object that can be iterated upon, meaning it has a
countable number of values. Examples of iterables are Lists, Tuples, Sets, and
Dictionaries--all the collections in Python.

The technical definition of an iterator in Python is that it conforms to the
_iterator_ protocol, meaning that it responds to `__iter__()` and `__next__()`.

## Iterators and Iterables: What's the Difference?

An _iterator_ is an object that can be iterated upon. An _iterable_ is a container
within which you can get an _iterator_. For example, a tuple is an iterable and
an iterator can be derived from it.

## Looping through an Iterator

You can loop through an iterable by first calling `iter()` to get the iterator, and
then calling `next()` to get each value. In practice, you'll use loops such as
*for loops* to iterate through, but this will inform how it works behind the scenes.

```python
# Using iter() and next()
my_tuple = (4, 5, 6)
my_iterator = iter(my_tuple)
print(next(my_iterator))
print(next(my_iterator))
print(next(my_iterator))

# Using a for loop
for val in my_tuple:
  print(val)
```

## Creating a Custom Iterator

Why would you create a custom iterator? One big reason is to design collections,
that when you loop through them, they save memory. For example, when reading files,
Python structures the action as an iteration, and data is read into memory
line by line. Here's how to create your own iterator:

```python
class NumberFeeder:
  # An iterator that keeps on counting upwards
  def __init__(self, start=0):
    self.num = start

  def __iter__(self):
    return self

  def __next__(self):
    num = self.num
    self.num += 1
    return num

nf = NumberFeeder()
# Keep printing the next value
print(next(nf))
print(next(nf))
print(next(nf))
```
