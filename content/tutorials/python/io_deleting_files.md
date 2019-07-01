---
title: "IO: Deleting Files"
date: 2019-06-23T22:38:39-04:00
draft: true
sort_key: 25
category: "Python"
---

# Python Deleting Files

Deleting a file in Python is done with a separate module, the `os` module.

*data.txt*
```python
import os
os.remove('data.txt')
```

## Check if a File or Folder Exists

You will get an error if you try to delete a file that doesn't exist, so it's
always best to check:

```python
import os
if os.path.exists('data.txt'):
  os.remove('data.txt')
else:
  print("Well, that's not going to work!")
```

## Deleting an Entire Folder

Deleting an entire folder is as simple as calling the `rmdir` method of `os`.

```python
import os
os.rmdir('logs')
# Make sure to check if the path exists before trying to delete!
```
