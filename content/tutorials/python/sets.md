---
title: "Sets"
date: 2019-06-23T22:05:30-04:00
draft: false
sort_key: 11
category: "Python"
---

# Python Sets

Python sets are similar to lists except that the values are *unordered* and
*duplicates are not allowed*.


When are they most useful?

## Creating a Set
Sets can be created using curly braces.

```python
carset = {'BMW', 'Mercedes', 'Porsche'}
print(carset)
```

NOTE: Sets are unordered, so you may not access values of a set by index like you can
with lists. However, you can look through a set since it is an iterable.

NOTE: Sets only contain unique items, so adding an item that already exists will
not work.

```python
carset = {'BMW', 'Mercedes', 'Porsche'}
for car in carset:
  print(car)
```

## Append items

You may append to a set using the `add()` or `update()` methods.

```python
carset = {'BMW', 'Mercedes', 'Porsche'}
carset.add('Audi')
print(carset)

carset.update(['VW', 'Opel'])
print(carset)
```

## Remove Items

Removing an item can be done by calling `remove()` with the set item as the argument.

```python
carset = {'BMW', 'Mercedes', 'Porsche'}
carset.remove('BMW')
print(carset)
```

## Set Methods

Python has quite a few methods that can be applied to sets.

| add()                         | Adds an element to the set                                                     |
|-------------------------------|--------------------------------------------------------------------------------|
| clear()                       | Removes all the elements from the set                                          |
| copy()                        | Returns a copy of the set                                                      |
| difference()                  | Returns a set containing the difference between two or more sets               |
| difference_update()           | Removes the items in this set that are also included in another, specified set |
| discard()                     | Remove the specified item                                                      |
| intersection()                | Returns a set, that is the intersection of two other sets                      |
| intersection_update()         | Removes the items in this set that are not present in other, specified set(s)  |
| isdisjoint()                  | Returns whether two sets have a intersection or not                            |
| issubset()                    | Returns whether another set contains this set or not                           |
| issuperset()                  | Returns whether this set contains another set or not                           |
| pop()                         | Removes an element from the set                                                |
| remove()                      | Removes the specified element                                                  |
| symmetric_difference()        | Returns a set with the symmetric differences of two sets                       |
| symmetric_difference_update() | inserts the symmetric differences from this set and another                    |
| union()                       | Return a set containing the union of sets                                      |
| update()                      | Update the set with the union of this set and others                           |
