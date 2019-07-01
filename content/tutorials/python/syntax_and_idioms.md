---
title: "Syntax And Idioms"
date: 2019-06-23T22:03:45-04:00
draft: false
sort_key: 3
category: "Python"
---
# Python Syntax and Idioms

Unlike the highly idiomatic syntax found in Ruby, ES6 Javascript, and some
other languages, Python has few idioms. Furthermore, the syntax is very
readable, and most functions are written nearly in plain English.

## Syntax

The most notable characteristics of Python syntax are:

* **Indentation:** Blocks (aka functions) and control flow (if, while, for loops)
are delineated using indentation, rather than curly braces (C++, Java, C#, Javascript)
or do/end (Ruby).

* **Preference for snake case or no case:** Variable and function names with multiple words
prefer "snake casing" (similar to Ruby) or words being all fused together without spaces,
compared to the "camel casing" found in most other languages (Javascript, C++, Java).
Classes should be in Pascal Case, and constants should be in upper snake case.

* **No semicolons needed:** End of line statements do NOT need to be terminated by
colons. If you want to have multiple statements on the same line however, you
may use semicolons to separate them.

* **Overflowing lines can be split up using a backslash:** If you have a line that
is getting too long, you may break it up using the "\" character.


```python
# Showcase of the clean indentation found in python
class Train:
  def top_speed(name):
    if name == 'Shinkansen':
      return 320 #km/h
      # .
      # .
      # .
```

Besides the above rules (especially "Indentation"), few rules exist for Python
code syntax.

## Idioms

Python may not be an opinionated (and idiom-riddled) language (compared to, say, Ruby),
however, some guidelines exist for writing "good" Python code, and some idioms
will help speed up your programming as well.

* **Chained comparison operators:** Be wary of putting too many logical operators
(AND, OR) in your conditional statements.

* **Underscores:** Fill this in

* **Use Falsy & Truthy:** Rather than compare directly to `True` and `False` (e.g. `if x == True`),
aim to compare to Truthy or Falsy (e.g. `if x`) instead.

* **The "in" keyword:** In some other languages, you might be used to calling a method
on an array like `.include?` or `.contains` but in Python use the `in` keyword. Use for example,
`country in {'Germany', 'Belgium', 'Netherlands'}` to know whether an item is in a set.

* **Python's Unique Ternary operator:** In other languages, you may be used to the `condition ? a : b`
ternary operator. In Python, a similar operator exists, and it looks like this: `do_something if condition else do_something_else`

* **Mutliple Assignment:** You can assign multiple variables at once by using commas.
For example, `x, y = 5, 4` will assign both x and y.

* **and instead of &&:** You may be used to double ampersands and double pipes from
other languages, but in Python you literally spell out "and" and "or".
