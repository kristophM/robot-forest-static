---
title: "Regex"
date: 2019-06-23T22:33:32-04:00
draft: false
sort_key: 19
category: "Python"
---

# Python RegEx

Python is really good at handling regular expressions ("RegEx") and has a built-in
module called `re`.

## Check if a String Contains a Matching Substring

The regex `search()` method allows us to search for substrings matching the regex
search criteria.

```python
import re
txt = "3 blind mice"
# Check to see if the string contains a number
x = re.search("\d", txt)
```
## Locate the Range of a Substring Within a String

```python
import re
txt = "You can contact Arthur at am@mgn.net"
# Check to see if the string contains a number
x = re.search("\w+@(\w|\.)+\s*", txt)
print(x.span())
```

## Useful Regex Functions

| Function | Description                                                       |
|----------|-------------------------------------------------------------------|
| findall  | Returns a list containing all matches                             |
| search   | Returns a Match object if there is a match anywhere in the string |
| split    | Returns a list where the string has been split at each match      |
| sub      | Replaces one or many matches with a string                        |

## Metacharacters and Sets

The following metacharacters and sets can be used to build regular expressions.


| [abc]    | A single character of: a, b, or c               |
|----------|-------------------------------------------------|
| [^abc]   | Any single character except: a, b, or c         |
| [a-z]    | Any single character in the range a-z           |
| [a-zA-Z] | Any single character in the range a-z or A-Z    |
| ^        | Start of line                                   |
| $        | End of line                                     |
| \A       | Start of string                                 |
| \z       | End of string                                   |
| .        | Any single character                            |
| \s       | Any whitespace character                        |
| \S       | Any non-whitespace character                    |
| \d       | Any digit                                       |
| \D       | Any non-digit                                   |
| \w       | Any word character (letter, number, underscore) |
| \W       | Any non-word character                          |
| \b       | Any word boundary                               |
| (...)    | Capture everything enclosed                     |
| (a|b)    | a or b                                          |
| a?       | Zero or one of a                                |
| a*       | Zero or more of a                               |
| a+       | One or more of a                                |
| a{3}     | Exactly 3 of a                                  |
| a{3,}    | 3 or more of a                                  |
| a{3,6}   | Between 3 and 6 of a                            |
