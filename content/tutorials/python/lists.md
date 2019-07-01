---
title: "Lists"
date: 2019-06-23T22:05:08-04:00
draft: false
sort_key: 9
category: "Python"
---

# Python Collections
Python allows for 4 types of collections: *list*, *tuple*, *set*, and *dictionary*.

|            | Ordered? | Can change values? | Allows duplicates? |
|------------|----------|--------------------|--------------------|
| List       | Yes      | Yes                | Yes                |
| Tuple      | Yes      | No                 | Yes                |
| Set        | No       | No                 | No                 |
| Dictionary | No       | Yes                | No                 |

# Lists

Lists are *ordered* collections of values, which can be changed. Python
doesn't ship with native support for arrays, but lists work fine for most
applications.

NOTE: In Python, lists are what most people think of arrays in other languages (Javascript,
Ruby, etc.), but arrays (in Python) have a more mathematical definition. For example,
if you multiplied `3` by an *array* of `[1, 2, 3]`, you would get `[1, 6, 9]`. But
if you tried the same operation with a *list*, you would get an error. For more information
on arrays in Python, take a look at the <a href="{{< ref "/tutorials/numpy/getting_started.md">}}">Numpy Section</a>

## Creating a List

To create a list, just use square bracket ("[]") notation.

```python
# Numerical list
x = [4, 5, 6]
print(x)
# String list
y = ['Marie', 'Hannes', 'Dirk']
print(y)
# List of mixed type
z = ['apples', 345, 4.7e-2]
print(z)
```

Note: Arrays can be of mixed type in Python!

## Accessing Values or Slices

To access a value of the list, use the bracket notation ("[]") along with the index.
Python lists are zero indexed as in most programming languages.

```python
x = [4, 50, 7.3]
# Access the first element
print(x[0])
# Access the last element.
print(x[-1])
```
To access a *slice* (or "subsection"), you also use the bracket notation and
specify a range.

```python
x = [4, 50, 7.3, 9, 1, 0, 8]

# The first 3 elements
print(x[0:3])

# Trick: You can leave out the zero for brevity
print(x[:3])

# The last 3 elements
print(x[(len(x) - 3):])
```

### Get the length of a list

Use the `len()` function.

```python
x = [2, 4, 3]
print(len(x))
```

## Iterate Through a List

Since lists are a form of _collection_, you may use a _for loop_ to iterate through
them.

```python
x = [2, 4, 3]
for e in x:
  print(e)
```

## Pushing and Popping a List

To add or remove items to and from a list, you may use the `append()` and `pop()`
methods.

```python
x = [2, 4, 9]
print("List before changes: ", x)

# Append to array
x.append(0)
print("List after appending: ", x)

# Remove last value of array
x.pop()
print("List after popping off last value: ", x)

# Remove the first element of the array
x.pop(0)
print("List after popping off first value: ", x)
```

## Other Useful List Functions

You may find that you frequently use these methods when working with lists in Python:

| Method    | Description                                                                  |
|-----------|------------------------------------------------------------------------------|
| append()  | Adds an element at the end of the list                                       |
| clear()   | Removes all the elements from the list                                       |
| copy()    | Returns a copy of the list                                                   |
| count()   | Returns the number of elements with the specified value                      |
| extend()  | Add the elements of a list (or any iterable), to the end of the current list |
| index()   | Returns the index of the first element with the specified value              |
| insert()  | Adds an element at the specified position                                    |
| pop()     | Removes the element at the specified position                                |
| remove()  | Removes the first item with the specified value                              |
| reverse() | Reverses the order of the list                                               |
| sort()    | Sorts the list                                                               |

## Some Common Operations

Below are some additional operations with more advanced functionality.

### Sorting by a function

```python
x = [{"a": 7, "b": 5}, {"a": 2, "b": 5}, {"a": 4.9, "b": 0}]
x.sort(key=lambda e: e["a"])
```

### Determining what values two arrays have in common (overlap)

Python does not have a built in method for this, but you can use the fact that *sets*
in Python may not contain duplicate values, and use the *bitwise AND* operator to
take the intersection of the two sets.

```python
x1 = [1, 3, 4, 6, 8]
x2 = [1, 0, 4, 6.5, 9.]
intersection = list(set(x1) & set(x2))
print(intersection)
```
