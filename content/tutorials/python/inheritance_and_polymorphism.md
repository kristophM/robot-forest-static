---
title: "Inheritance and Polymorphism"
date: 2019-06-23T22:20:25-04:00
draft: true
sort_key: 15
category: "Python"
---

# Python Inheritance

Python supports inheritance, as well as multiple inheritance. Inheriting from an
existing class is easy.

## Syntax

```python
class MusicalInstrument:
  def __init__(self, name, musical_key):
    self.name = name
    self.musical_key = musical_key

  def printInfo(self):
    print("The key of this", self.name, "is", self.musical_key)

class Saxophone(MusicalInstrument):
  pass

alto_sax = Saxophone('Alto Saxophone', 'Eb')
alto_sax.printInfo()
```

## Overrides and Polymorphism

Polymorphism means an object can take many forms. Python supports polymorphism
in several ways. One can see easily that methods on the class, including the
initialization method, can be overwritten without any special "override" annotation.

```python
class Saxophone(MusicalInstrument):
  def __init__(self, name, musical_key, reed_type):
    super(Saxophone, self).__init__(name, musical_key) # Call parent class init
    self.reed_type = reed_type # Add new child class property

  def printInfo(self):
    # Override printInfo() method
    print("The key of this", self.name, "is", self.musical_key, "and uses a", self.reed_type, "reed")

alto_sax = Saxophone('Alto Saxophone', 'Eb', 'natural')
alto_sax.printInfo()
```

Note 1) that the `__init__` function calls the parent's init function using `super()`
and then adds in a new attribute, and 2) that the child class overrides the `printInfo()`
model as well.

## Public, Private, and Protected Methods

Python doesn't have the classic `private`, `public`, and `protected` prefixes
on method and variable declarations that we are used to in other languages.
Instead, Python observes the convention of prefixing variables and functions with
a single underscore ("\_") to make variables and methods *protected*, and double underscores ("\_\_")
to make them *private*.

### Protected members

Protected members of a class are accessible from within the class and are also available to its sub-classes.

```python
class employee:
    def __init__(self, name, sal):
        self._name=name  # protected attribute
        self._salary=sal # protected attribute
e1=employee("Yan", 10000)
e1._salary # returns 10000
e1._salary=20000
e1._salary # returns 20000
```

### Private members

Private members of a class are only accessible from methods within the class itself.

```python
class employee:
    def __init__(self, name, sal):
        self.__name=name  # private attribute
        self.__salary=sal # private attribute
e1=employee("Michael",10000)
e1.__salary # AttributeError: 'employee' object has no attribute '__salary'
```
