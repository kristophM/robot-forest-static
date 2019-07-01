---
title: "IO: File Handling"
date: 2019-06-23T22:38:04-04:00
draft: false
sort_key: 23
category: "Python"
---

# Python File Handling

Python has extensive methods for handling files and working with the filesystem
without the need for other libraries.

## Opening Files

The act of opening a file loads the content of the file into memory. In Python
you have the option of either loading the file as binary or as text.

```python
# Open a file as text
text_file = open('notes.txt')
# Open a file as binary
binary_file = open('profile_photo.jpg', 'b')
```

### Modes for Opening a File

Files can be opened with different interaction modes, namely regarding reading
and writing permissions.

* *'r':* - Read - the default value, which opens a file for reading only, and returns
an error if the specified file cannot be located.

* *'a':* - Append - opens a file to add on to pre-existing content. If the file
doesn't exist, it creates it.

* *'w':* - Write - opens a file to write to it. It creates the file if the path
doesn't exist.

* *'x':* - Create - creates a file, and returns an error if the file already exists.

NOTE: The ability to perform these actions also depends on the file permissions
from your operating system for the directory/files you're working with.

## Closing Files

Some files can be very large, and it's a good idea to close files to remove their
contents from memory and thus prevent bloating. To do so, use the `close()` method
when you're done working with a file.

```python
text_file = open('notes.txt')
# ... do stuff ...
# then close it.
text_file.cose()
```
