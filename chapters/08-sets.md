# Chapter 08 - Sets

---

## Introduction
* Stores multiple items in a single variable.
* A collection that is unordered and unindexed.
* Written with curly brackets.

```python
setObj = {"Cat", "Dog", "Rabbit", "Bear", "Mouse"}
print(setObj)
```

## Unordered
* Even if the items are written in a given order, the values of the set themselves are unordered.
* When accessing a set, the order of values will be different each time.

```python
# While the numbers are written here in order, the actual output will be random.

setObj = {1, 2, 4, 6, 7, 8, 15, 25, 27, 33, 34, 41, 55, 65, 67, 80, 86, 91, 92, 96}
print(setObj)
```

## Other Stipulations
* Items are unordered and cannot be changed.
* Duplicate values are not allowed.
* Items can be any data type.
* The `len()` method retrieves the number of items. Same as with lists and tuples.

## Accessing Items
* You cannot access individual items of a set with an index or key.
	* Use a `for` loop to iterate over items.
	* Use the `in` keyword to check if a particular value is in the set.

```python
setObj = {"Cat", "Dog", "Rabbit", "Bear", "Mouse"}

# Iterate over items.
for animal in setObj:
  print(animal)

print("")
print("---")
print("")

# Check individual item.
if "Dragon" in setObj:
  print("Dragons are real")
else:
  print("Dragons do not exist")
```

## Add New Items
* Once a set has been created, you cannot change it's items.
* However, you can still add new items onto the set.
* To add one new item, use the `add()` method.

```python
setObj = {"Cat", "Dog"}
setObj.add("Rabbit")
print(setObj)
```

## Concat
* To add a collection onto the set, use the `update()` method.
	* Can be used to add multiple items at once.
	* Accepts tuples, lists and dictionaries. Not just other sets.

```python
setObj = {"Cat", "Dog"}
newItems = {"Rabbit", "Bear", "Mouse"}
setObj.update(newItems)
print(setObj)
```

## Remove Item
* There are two methods for this, `update()`, and `discard()`.
* The difference is that:
	* `update()` raises an error if the item does not exist.
	* `discard()` does not raise an error.

```python
setObj = {"Cat", "Dog", "Rabbit", "Bear", "Mouse"}

setObj.remove("Mouse")
setObj.discard("Dog")

print(setObj)
```

## Join - Union
* The `union()` method is used to combine two sets into a new object.
* In other words, it contains items from both sets.

```python
setA = {"Cat", "Dog", "Rabbit", "Mouse", "Bear"}
setB = {"X", "Y", "Z"}
setC = setA.union(setB)

print(setC)
```

## Join - Intersection
* The `intersection()` method returns a new set consisting of items in both input sets.
	* Items that are in both sets.
	* x AND y
* You can also use the 'intersection_update' method to do this without creating a new object.

```python
setA = {1, 3, 4, 5, 7, 8, 11, 14, 15, 19}
setB = {1, 2, 4, 9, 11, 15, 16, 17, 18, 20}
setC = setA.intersection(setB)

print(setC)
```

## Join - Symmetric
* The `symmetric_difference()` method returns a new set consisting of items that are only in one input set.
	* Items from one or the other, but not both.
	* x OR y
* You can also use the `symmetric_difference_update()` method to do this without creating a new object.

```python
setA = {4, 6, 7, 8, 10, 12, 14, 15, 16, 17}
setB = {1, 2, 3, 4, 6, 7, 8, 13, 14, 19}
setC = setA.symmetric_difference(setB)

print(setC)
```

## Methods Table
| Method | Description |
|---|---|
| add() | Adds new item to set. |
| clear() | Removes all items from set. |
| copy() | Returns a copy of the set, cloning it. |
| difference() | Returns a set containing the difference between multiple sets. |
| difference_update() | Removes items from a set that are also in another given set. |
| discard() | Removes given item without error. |
| intersection() | Returns a new set consisting of items in both input sets. |
| intersection_update() | Same as 'intersection()', but in-place. |
| isdisjoint() | Returns if two sets have an intersection. |
| issubset() | Returns whether all items in a given set are contained in another set. |
| remove() | Removes given item. If it does not exist, there will be an error. |
| symmetric_difference() | Returns a new set consisting of items that are only in one input set. |
| symmetric_difference_update() | Same as ' symmetric_difference', but in-place. |
| union() | Combines two sets into a new object. |
| update() | Concats items onto set from given collection. |

---

**Previous:** [07 - Tuples](./07-tuples.md)  
**Next:** [09 - Dictionaries](./09-dictionaries.md)

[Contents](./readme.md)