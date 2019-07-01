---
title: "JSON"
date: 2019-06-23T22:33:15-04:00
draft: true
sort_key: 18
category: "Python"
---
# Python JSON

Python includes a built-in module called `json` that can be used to work with JSON
data.

## Parsing JSON

To convert a JSON string to a python dictionary, use the `json.loads()` method.

```python
import json
# A JSON string
data_string = "{\"id\":1,\"user_id\":6,\"photo_id\":5,\"created_at\":\"2019-02-12T04:26:15.115Z\",\"updated_at\":\"2019-02-12T04:26:15.115Z\"}"

# Convert to Dictionary
data_dict = json.loads(data_string)

# Print the value of one of the dictionary keys
print(data_dict['user_id'])
```

## Converting Dictionaries to JSON

To convert from Python dictionaries to JSON, use the `dumps()` method.

```python
import json
record = dict(id=1, user_id=6, photo_id=5, tags=["street", "buildings", "cafe"])
record_json_str = json.dumps(record)
print(record_json_str)
```
NOTE: Python converts Python objects to their respective JSON equivalents. For example,
_list_ and _tuple_ objects become JSON arrays, while _dict_ objects become JSON
objects, etc.

### Formatting JSON strings
To achieve "pretty print" of JSON, rather than simply a big, long, unreadable string,
use the `indent=` parameter.

```python
import json
record = dict(id=1, user_id=6, photo_id=5, tags=["street", "buildings", "cafe"])
record_json_str = json.dumps(record, indent=4)
print(record_json_str)
```
