---
title: "Classes and Objects"
date: 2019-06-23T22:20:25-04:00
draft: true
sort_key: 15
category: "Python"
---

# Python Object Oriented Programming

In Python nearly everything is an object, and thus has methods and properties.
Let's learn to create our own using classes.

## Create a Class

To create a class in Python, you use the `class` keyword.

```python
class Car:
  num_wheels = 4
```

## Instantiate an Object

To create a new instance of class `Car`, we follow the name of the class with parentheses.

```python
car = Car()
print(car.num_wheels)
```

## The __init__ Initialization Block

Every class can be initialized with certain values. This happens within the special
`__init__` function that Python calls for every new instantiation of a class.

```python
# Define a class Car
class Car:
  def __init__(self, brand_name):
    self.brand_name = brand_name
    # Also do any other actions that need to happen upon initialization here

car = Car("Volvo")
print(car.brand_name)
```


## Object Methods

Functions that act upon particular objects are called "methods." To create a method,
or "instance method" as known in other programming languages, define a function

```python
# Define a class Car
class Car:
  def __init__(self, brand_name):
    self.brand_name = brand_name
    # Also do any other actions that need to happen upon initialization here

  def print_brand(self):
    print(self.brand_name)

car = Car("Volvo")
car.print_brand()
```

### Self

The `self` keyword in Python is similar to the `self` and `this` keywords found
in other languages that describe the current object context. It does not need to be
called "self", and can be defined as any string in the first argument of the function.
The above could be re-written as:

```python
class Car:
  def __init__(abc, brand_name):
    abc.brand_name = brand_name

  def print_brand(xyz):
    print(xyz.brand_name)
```

## Static (Class) Methods

Sometimes we want to create methods that apply to an entire class, rather than
just its objects. For example, to determine the number of cars that exist, we may
want a class method on `Car`. This can be done with the `@staticmethod` decorator.

```python
class Car:
  @staticmethod
  def count_cars():
    return 50

print(Car.count_cars())
```

Notice that there is no `self` argument, because it's no longer needed. 

## Modify Object Properties

No explicit attribute accessor is needed to update a Python object property. You can
simply assign the property directly:

```python
car.brand_name = "Mercedes"
```

### Delete Object Properties

The `del` function is used to delete a property from an object. To remove the
`brand_name` property from the `car` object, simply use the `del` command:

```python
del car.brand_name
```

Note that if you try to run car.brand_name, Python will complain that
the property no longer exists!

If you instead want to simply clear a property, set the property to `None`:

```python
car.brand_name = None
```
