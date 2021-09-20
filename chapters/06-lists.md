# Chapter 06 - Lists

---

## Introduction
* Used to store multiple items in a single variable.
* Stores collection of data.
* Defined using square brackets.
* Similar to arrays in other languages.

```python
exampleArray = ['X', 123, 'Y']
print(exampleArray)
```

## List Items
* Items in the list have a defined order.
* Items can be added, removed, or changed as needed.
* Duplicate values are allowed.
* Each item has an index number. (Starting at Zero)
* New items are placed at the end of the list.
* List items can be any data type. They do not all have to be the same.

## List Length
Similar to strings, the 'len' function retrieves the list length.

```python
arrayObj = ["X", "Y", "Z"]
arrayLength = len(arrayObj)
print(arrayLength);
```

## Access Elements
* List items are indexed. You can access an item by referring to its index number.
	* Remember that the first item has index 0

```python
arrayObj = [2, 4, 8, 16, 32, 64, 128]
chosenElement = arrayObj[3]
print(chosenElement)
```

## Access Negative
* This means starting from the end.
	* -1 refers to the last item.
	* -2 refers to second last.
	* *etc*

```python
arrayObj = [128, 256, 512, 1024, 2048, 4096]
lastElement = arrayObj[-1]
secondLastElement = arrayObj[-2]

print(lastElement)
print(secondLastElement)
```

## Sub-Array
* You can extract part of an array by specifying a range of index numbers.
* The range will retrieve a new list object with those items.
* Similar to sub-strings.

```python
baseArray = [1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096, 8192, "..."]

subStart = baseArray[:4]
subGeneralA = baseArray[4:7]
subGeneralB = baseArray[7:10]
subEnd = baseArray[10:]

print(subStart)
print(subGeneralA)
print(subGeneralB)
print(subEnd)
```

## Negative Sub-Array
Specify negative index numbers to extract elements from the end of the list.

```python
baseArray = [1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096, 8192, "..."]
negativeSub = baseArray[-5:]
print(negativeSub)
```

## Includes
Use the 'in' keyword to check if a given item is included in the list.

```python
arrayObj = ["ABC", "DEF", "GHI", "JKL", "MNO", "PQRS", "TUV", "WXY", "Z"]
inclStatus = bool("XYZ" in arrayObj)
print(inclStatus)
```

## Change Elements
To change element values, refer to the index.

```python
arrayObj = [1, 2, 3]
arrayObj[1] = 5
print(arrayObj)
```

## Insert
* Use the 'insert' method to add a new list item to a specified index.
	* Inserting an item at a specified index.

```python
arrayObj = ["Cat", "Dog", "Rabbit"]
arrayObj.insert(2, "Mouse")
print(arrayObj)
```

## Append
The 'append' method adds an item to the end of the list.

```python
arrayObj = ["Cat", "Dog", "Rabbit"]
arrayObj.append("Bear");
print(arrayObj)
```

## Remove Item
* The 'remove' method removes any list items of that given value.
* All instances of the value are removed.

```python
arrayObj = ["Cat", "Dog", "Rabbit", "Dog", "Bear", "Mouse"]

arrayObj.remove("Dog")
arrayObj.remove("Mouse")

print(arrayObj)
```

## Remove Index
* The 'pop' method removes the list item at the given index.
* If no index is given, the last item is removed by default.

```python
arrayObj = ["Cat", "Dog", "Rabbit", "Bear", "Mouse"]

arrayObj.pop(1)
arrayObj.pop()

print(arrayObj)
```

## Clear
The 'clear' method empties the list.

```python
arrayObj = [1, 2, 3]
arrayObj.clear()
print(arrayObj)
```

## For Each
You can loop through list items using a 'for' loop.

```python
arrayObj = ["Cat", "Dog", "Rabbit", "Mouse", "Bear"]

for animal in arrayObj:
  print(animal)
```

## Sorting
* The 'sort' method is used to sort list items.
	* Ascending order by default.
	* To sort descending, add the keyword argument: 'reverse = True'

```python
# Define arrays
stringArray = ["Cat", "Dog", "Rabbit", "Mouse", "Bear"]
numberArray = [5, 14, 8, 9, 19]

# Sort animals from A-Z
stringArray.sort()
print(stringArray)

# Sort animals from Z-A
stringArray.sort(reverse = True)
print(stringArray)

# Sort numbers ascending
numberArray.sort()
print(numberArray)

# Sort numbers descending
numberArray.sort(reverse = True)
print(numberArray)

# Done
```

## Sort by Function
To use a function to determine sort order, add the keyword argument: 'key = \[functionName\]'

```python
def sortFunction(n):
  return abs(n - 50)


arrayObject = [35, 47, 46, 12, 40, 36, 5, 4, 41, 19]
arrayObject.sort(key = sortFunction)
print(arrayObject)
```

## Case-Insensitive Sort
To remove case-sensitivity when sorting a list of strings, use 'str.lower' as the key function.

```python
stringArr = ["CaT", "dOg", "RaBbIt", "bEaR", "MoUsE"]
stringArr.sort(key = str.lower)
print(stringArr)
```

## Reverse
To reverse the order of list items, use the 'reverse' method.

```python
arrayObj = [33, 16, 34, 24, 2, 31, 5, 25, 42, 35, 39, 23, 47, 27, 36, 1, 8, 41, 46, 21]
arrayObj.reverse()
print(arrayObj)
```

## Clone
To clone a list, use the 'list' method.

```python
origArr = [1, 2, 3]
clonedArr = list(origArr)
print(clonedArr)
```

## Concat
* Two ways of joining lists together:
	* Adding them like you would with numbers.
	* Using the 'extend' method to append one list onto another.

```python
# Adding

numListA = [39, 37, 26, 1, 25, 12, 43, 50]
numListB = [27, 26, 47, 45, 20, 40, 37, 7]
numListC = [7, 44, 15, 29, 21, 11, 33, 37]

combinedNumbers = numListA + numListB + numListC
print(combinedNumbers)

# -----------------

# Extending

strListA = ["Cat, Dog", "Rabbit"]
strListB = ["Bear", "Bird", "Fish"]

strListA.extend(strListB)
print(strListA)
```

## Methods Table
| Method | Description |
|---|---|
| append() | Adds an element to the end of the list. |
| clear() | Removes all elements. |
| copy() | Returns separate copy of the list, cloning it. |
| count() | Returns number of elements with given value. |
| extend() | Adds a given list to the end of the current list. |
| index() | Returns index of first element with given value. |
| insert() | Adds element at specified index. |
| pop() | Removes element at specified index. |
| remove() | Removes elements that are the given value. |
| reverse() | Reverses list order. |
| sort() | Sorts list items. |


---

**Previous:** [05 - Operators](./05-operators.md)  
**Next:** [07 - Tuples](./07-tuples.md)

[Contents](./readme.md)