---
title: "Dictionaries"
date: 2019-06-23T22:19:55-04:00
draft: false
sort_key: 12
category: "Python"
---

# Python Dictionaries

Dictionaries are collections of key-value pairs, which are *unordered* and *changeable*.
In other languages, dictionaries may be known as hashes (Ruby), maps (Go),
HashMaps (Java), or objects (JavaScript).

When are they most useful? When elements in your collection need to be labeled.

## Creating a Dictionary

A dictionary can be constructed either by using curly braces (similar to javascript objects),
or using the `dict()` constructor.

```python
# Curly brace method
lightbulb = {"brand": "GE", "socket_type"="E45", "wattage": 45}
# dict() constructor
lightbulb = dict(brand="GE", socket_type="E45", wattage=45)
```

Note: The values do not always have to be the same type. Above you see both numbers and
strings.

# Accessing a Value

To access a value by its key, simply use square braces ("[]").

```python
lightbulb = {"brand": "GE", "socket_type"="E45", "wattage": 45}
wattage = lightbulb["wattage"]
```

# Adding a Value

Adding a value is similar to accessing a value. Use square braces.

```python
lightbulb = {"brand": "GE", "socket_type"="E45", "wattage": 45}
lightbulb["price"] = 5.99
print(lightbulb)
```

# Removing a Value

To remove a value, use the `pop` method or the `del` method. To clear the entire
dictionary, use the `clear()` method.

```python
lightbulb = {"brand": "GE", "socket_type"="E45", "wattage": 45}
del lightbulb["brand"]
lightbulb.pop("socket_type")
print(lightbulb)

lightbulb.clear()
print(lightbulb)
```

# Check if a Key Exists

At times you will want to know if a dictionary contains a certain key. This is where
the `in` keyword comes in handy.

```python
d = dict(x=5, y=7)
print("z" in d) # returns False
print("x" in d) # returns True
```

## Copy a Dictionary

Since dictionaries are passed by reference rather than values (think pointers in other languages),
you may want to make copies of them to prevent overwriting of the original data.
To copy a dictionary, just use the constructor function, `dict()`.

```python
d = {"x": 5, "y": 7}
new_dict = dict(d)
print(new_dict)
```

## Dictionary Methods

The following methods are popular for interacting with dictionaries.

| Method       | Description                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| clear()      | Clears the dictionary                                                                                       |
| fromkeys()   | Returns a subset of the dictionary with the specified keys and values                                       |
| get()        | Returns the value of the specified key                                                                      |
| items()      | Returns a list containing the a tuple for each key value pair                                               |
| keys()       | Returns a list containing the dictionary's keys                                                             |
| pop()        | Removes the element with the specified key                                                                  |
| popitem()    | Removes the last inserted key-value pair                                                                    |
| setdefault() | Returns the value of the specified key. If the key does not exist: insert the key, with the specified value |
| update()     | Updates the dictionary with the specified key-value pairs                                                   |
| values()     | Returns a list of all the values in the dictionary                                                          |
