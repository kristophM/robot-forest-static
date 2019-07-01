---
title: "Modules"
date: 2019-06-23T22:33:02-04:00
draft: true
sort_key: 17
category: "Python"
---

# Python Module Organization

*Modules* help organize code into distinct sections. They can be thought of
as separate libraries of code encapsulated into an object that can be imported
in other code.

## Create a Module

To create a module, you save code in a Python file.

Note: The file name is important because this will be the name of the module

```python
# Save this code in a file called robotnames.py
def get_names():
  return ['R2D2', 'C3PO', 'HAL', 'Doraemon']
```

## Import a Module

To import a module, simply use the `import` command.

```python
import robotnames

names = robotnames.get_names()
print(names)
```
### Renaming a Module

Often it's a good practice renaming modules into something more manageable.

```python
import robotnames as rn
names = rn.get_names()
print(names)
```

## Variables in a Module

Functions aren't the only things that can be stored in a module. You may also
store variables!

```python
# Save this in a module file called robotnames.py
ROBOT_COUNT = 305
```

```python
# Now, from another Python file/terminal, run the following:
import robotnames as rn
print(rn.ROBOT_COUNT)
```

## Importing Only Certain Attributes of a Module

Let's take Python's built in "platform" module as an example. You can use the
`dir()` function to list out all the defined function and variable names inside of a
module.

```python
import platform
print(dir(platform))
```

Now let's say we're interested in the `python_compiler` function from that module.
We can import only that function from the module as to not bloat our code, using
the `from` keyword. 

```python
from platform import python_compiler

print(python_compiler())
```
