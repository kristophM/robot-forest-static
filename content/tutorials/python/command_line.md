---
title: "Command Line"
date: 2019-06-23T22:35:32-04:00
draft: false
sort_key: 21
category: "Python"
---

# Interacting with the Command Line via Python

At times, you may want Python to communicate with the system, just as if you
were typing something into a Bash shell in a terminal window.

For example, you may want to:

* Run an executable from the command line since the program is not written
in Python

* Change the access permissions for a file or folder on the system

* Prompt the user for input (if you are writing a command line program)

## Executing Command Line Instructions

If you would like to communicate with the operating system, read/write files, and
run programs from the shell, it's possible to run shell commands directly from
Python, using the built-in `subprocess` module.

```python
bashCommand = "ls" # A unix shell command for listing the contents of a directory
import subprocess
process = subprocess.Popen(bashCommand.split(), stdout=subprocess.PIPE)
output, error = process.communicate()
```

The `output` variable above, if the command was successful, stores the output
of the command. Otherwise, the error variable stores the error output.

## Prompt User Input From the Command Line

Prompting user input is as simple as using the `input()` function. Suppose you
want to ask the user their name before continuing through the rest of the script:

```python
print("How much would you like to withdraw?")
amt = input()
print("Here is $", amt)
```
