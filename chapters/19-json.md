# Chapter 19 - JSON

---

## Introduction
* Syntax for storing and exchanging data.
* Consists of text, written in **J**ava**S**cript **O**bject **N**otation.
* Python has a built-in module 'json' which is used to work with JSON data.

## Usage
* To parse a JSON string into an object, use the `json.loads()` method.
* To stringify an object into JSON text, use the `json.dumps()` method.
* When you convert from Python to JSON, Python data types are converted into their JSON equivalent.

## Type Conversion
| Python | JSON |
|---|---|
| dict | Object |
| list | Array |
| tuple | Array |
| str | String |
| int | Number |
| float | Number |
| True/False | Boolean |
| None | null |

## JSON Methods
|  | Node JS | Python |
|---|---|---|
| String --> Object | `JSON.parse()` | `json.loads()` |
| Object --> String | `JSON.stringify()` | `json.dumps()` |

## Example - Parse

```python
import json

# some JSON:
x = '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x)

# the result is a Python dictionary:
print(y["age"])

```

## Example - Stringify

```python
import json

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)

```

## Stringify Format
* When printing a JSON string as-is, it has no line breaks or indentation.
	* Therefore, it is not easy to read.
* The 'json.dumps()' method has parameters to:
	* Specify the number of indents so that the text is easier to read. (indent=4)
	* Order the keys in a result. (sort_keys=True)

```python
import json

preparedObject = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

outputText = json.dumps(preparedObject, indent=4, sort_keys=True)
print(outputText)
```


---

**Previous:** [18 - Math](./18-math.md)  
**Next:** [20 - Regular Expressions](./20-regex.md)

[Contents](./readme.md)