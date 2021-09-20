# Chapter 18 - Math

---

## Minimum and Maximum
* The `min()` and `max()` functions are used to find the lowest or highest number in an iterable.
* You can enter a series of numbers, or an existing collection.
* This example uses a 'set' object for input.

```python
numberSet = (49, 51, 2, 11, 93, 4, 10, 23, 27, 67, 78, 6, 81, 16, 13, 47, 72, 29, 19, 45)

minValue = min(numberSet)
maxValue = max(numberSet)

dispTxt = "{0} - {1}".format(minValue, maxValue)
print(dispTxt)
```

## Other Built-in Functions
* The `abs()` function returns the absolute value of a number.
* The `pow(x,y)` function returns x to the power of y. `(x^y)`

```python
absoluteValue = abs(-12.34)
powerValue = pow(6, 3)

print(absoluteValue)
print(powerValue)
```

## Module Functions
* Some important components of the 'math' module:
	* `sqrt()` - Returns the square root of a number.
	* `ceil()` - Rounds number up to nearest whole.
	* `floor()` - Rounds number down to nearest whole.
	* `pi` - Returns PI constant. (~3.14)

## Random
* The built-in module 'random' can be used to generate random numbers.
* This example displays three random numbers between 1 and 10.

```python
import random

genIndex = 0
currentValue = -1

for genIndex in range(3):
  currentValue = random.randrange(1, 11)
  print(currentValue)

print("Finished")
```

---

**Previous:** [17 - Datetime Module](./17-datetime.md)  
**Next:** [19 - JSON](./19-json.md)

[Contents](./readme.md)