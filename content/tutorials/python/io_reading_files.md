---
title: "IO: Reading Files"
date: 2019-06-23T22:38:23-04:00
draft: true
sort_key: 24
category: "Python"
---
# Python Reading Files

Once you've opened a file, you may read it using Python's built-in `read()` function.

*telegram.txt*
```
The quick brown fox jumped over the lazy dog's back.
```

```python
f = open('telegram.txt', 'r')
print(f.read())
# read only the first 50 characters:
print(f.read(50))
```
