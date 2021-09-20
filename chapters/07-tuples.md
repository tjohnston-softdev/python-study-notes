# Chapter 07 - Tuples

---

## Introduction
* Stores multiple items in a single variable.
* A collection that is ordered and static.
	* Think of it as a constant array.
* Written using round brackets.

```python
exampleTuple = ("Cat", "Dog", "Rabbit", "Mouse", "Bear")
print(exampleTuple)
```

## Stipulations
* Items are ordered and cannot be changed.
* Duplicate values are allowed.
* Indexing is performed the same as lists.
* The 'len' function is used to retrieve the tuple length.
* Items can be of any data type.

## Single Item Tuple
* To create a tuple with only one item, you must include a comma after said item.
	* Otherwise, Python will not recognise it as a tuple.
	* It will be interpreted as a separate value.

```python
# Correct
correctSingleTuple = ("Cat",)
correctType = type(correctSingleTuple)
print(correctSingleTuple)
print(correctType)

print("")

# Incorrect
incorrectSingleTuple = ("Dog")
incorrectType = type(incorrectSingleTuple)
print(incorrectSingleTuple)
print(incorrectType)
```

## Access
* Items in a tuple are accessed with index numbers.
* This is the same as with lists.

```python
tupleObj = ("Cat", "Dog", "Rabbit", "Mouse", "Bear")
indItem = tupleObj[2]
print(indItem)
```

## Includes
* Performed with the 'in' and 'not in' keywords.
* Same as with lists.

```python
fruitTuple = ("Apple", "Banana", "Orange", "Grape", "Watermelon")

if "Carrot" in fruitTuple:
  print("Carrot is a fruit")
else:
  print("Carrot is not a fruit")
```

## Changing Values
* Since items in a tuple are unchangeable, there is no immediate way to do this.
* What you can do is:
	* Convert the tuple into a list.
	* Change the values as needed.
	* Convert back into a tuple.

```python
def appendTuple(tObject):
  workList = list(tObject)
  workList += ["Bear", "Mouse"]
  return tuple(workList)

beforeTuple = ("Cat", "Dog", "Rabbit")
afterTuple = appendTuple(beforeTuple)

print("Before:")
print(beforeTuple)

print("")

print("After:")
print(afterTuple)
```

## Append Value
* There is one way to append values without any type conversion.
* You can add tuples together to contact them.

```python
tupleObj = ("Cat", "Dog")
print(tupleObj)

tupleObj += ("Rabbit", "Bear")
print(tupleObj)
```

## Looping
You can loop through items in tuples the same way you would with lists.

```python
tupleObj = ("Cat", "Dog", "Rabbit", "Bear", "Mouse")

for animal in tupleObj:
  print(animal)
```

## Methods
* 'count' returns the number of times a given value appears in the tuple.
* 'index' searches the tuple for a given value and returns the index of where it is first found.

---

**Previous:** [06 - Lists](./06-lists.md)  
**Next:** [08 - Sets](./08-sets.md)

[Contents](./readme.md)