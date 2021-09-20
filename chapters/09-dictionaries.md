# Chapter 09 - Dictionaries

---

## Introduction
* Stores data in 'key:value' pairs.
* Similar to JSON objects in JavaScript.
* A collection that is ordered and can be changed.
* While the values themselves can be duplicate, the keys must be unique.

```python
person = {
  "name": "John Smith",
  "year": 1882,
  "alive": False
}

print(person)
```

## Property Count
To retrieve the number of keys inside a dictionary, use the 'len' method.

## Access Properties
* You can read or change individual dictionary values by referencing the key in square brackets.
* In general, you can use dictionaries just like objects in JavaScript.

```python
jsonObject = {
  "name": "John Smith",
  "year": 1882,
  "alive": False
}

indValue = jsonObject["year"]
print(indValue)
```

## Keys and Values
* The 'keys' method returns a list of all keys in the dictionary.
* The 'values' method does the same, but for the key values.

```python
person = {
  "name": "John Smith",
  "year": 1882,
  "alive": False
}

keyList = person.keys()
valueList = person.values()

print(keyList)
print(valueList)
```

## Dictionary Views
* When using 'keys' and 'values', remember that they are only views to the dictionary.
	* Any changes to the original dictionary will be reflected in these objects.

```python
carObject = {
  "make": "Nissan",
  "model": "Skyline GTR",
  "year": 2002,
  "colour": "Blue"
}

keysView = carObject.keys()
valuesView = carObject.values()

print("Before:")
print(keysView)
print(valuesView)

carObject["model"] = "GT-R"
carObject["year"] = 2007
carObject["colour"] = "Grey"

print("")

print("After:")
print(keysView)
print(valuesView)
```

## Key Exists
Use the 'in' keyword to check whether a dictionary object has a particular key.

```python
person = {
  "name": "John Smith",
  "year": 1882,
  "alive": False
}

if "relationshipStatus" in jsonObject:
  print("Relationship status is known.")
else:
  print("Relationship status is unknown")


```

## Adding New Keys
This is done by assigning a value to a new index key.

```python
person = {
  "name": "John Smith",
  "year": 1882,
  "alive": False
}

person["relationshipStatus"] = "Widowed"
print(person)
```

## Remove Key
To do this, use the 'del' keyword on the dictionary key value.

```python
person = {
  "name": "John Smith",
  "year": 1882,
  "alive": False
}

print("Before:")
print(person)

del person["alive"]
print("")

print("After:")
print(person)
```

## Looping
You can loop through both the keys and values in a dictionary.

```python
person = {
  "name": "John Smith",
  "year": 1882,
  "alive": False
}

stringTemplate = "{0} = {1}"
currentLine = ""

for pKey, pValue in person.items():
  currentLine = stringTemplate.format(pKey, pValue)
  print(currentLine)

print("")
print("---")
```

## Cloning
To clone a dictionary object, use the 'copy' method.

```python
personA = {
  "name": "John Smith",
  "year": 1882,
  "gender": "Male",
  "alive": False,
  "cloned": False
}

personB = personA.copy()
personB["name"] = "Jane Smith"
personB["year"] = 1887
personB["gender"] = "Female"
personB["cloned"] = True

print(personA)
print(personB)
```

## Nesting
* Dictionaries can be nested.
	* Objects can contain objects.
	* Parent and Child.
* This is performed the same way as with JSON.

## Nesting Example 1
Lifted directly from [W3Schools](https://www.w3schools.com/python/python_dictionaries_nested.asp).

```python
myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}

print(myfamily)

```

## Nesting Example 2
Lifted directly from [W3Schools](https://www.w3schools.com/python/python_dictionaries_nested.asp).

```python
child1 = {
  "name" : "Emil",
  "year" : 2004
}
child2 = {
  "name" : "Tobias",
  "year" : 2007
}
child3 = {
  "name" : "Linus",
  "year" : 2011
}

myfamily = {
  "child1" : child1,
  "child2" : child2,
  "child3" : child3
}

print(myfamily)

```

## Methods Table
| Method | Description |
|---|---|
| clear() | Removes all 'key:value' pairs from dictionary. |
| copy() | Returns a copy of the dictionary object, cloning it. |
| items() | Returns a list containing a tuple object for each 'key:value' pair. Useful when iterating over properties. |
| keys() | Returns view list containing dictionary keys. |
| values() | Returns view list containing dictionary values. |


---

**Previous:** [08 - Sets](./08-sets.md)  
**Next:** [10 - Conditions](./10-conditions.md)

[Contents](./readme.md)