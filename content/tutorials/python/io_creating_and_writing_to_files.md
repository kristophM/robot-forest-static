---
title: "IO: Writing Files"
date: 2019-06-23T22:38:39-04:00
draft: true
sort_key: 25
category: "Python"
---

# Python Creating and Writing to Files

Writing to a file is as simple as opening an existing file or creating a new one,
using the correct modes, and then calling the `write()` method.

## Creating a New File

You can create a new file by first opening a file. You must open the file by
using the `x` (create), `a` (append), and `w` (write) modes.

```python
f = open('data.txt', 'w')
f.write('3 5 1 0 24')
f.close()

# Now read it!
f = open('data.txt', 'r')
print(f.read())
f.close()
```

## Writing to an Existing File

To write to an existing file, the logic is similar, but in a different mode.

*data.txt*
```
3 5 1 0 24
```

```python
f = open('data.txt', 'a')
f.write('0 3 8 2')
f.close()

# Now read it!
f = open('data.txt', 'r')
print(f.read())
f.close()
```
