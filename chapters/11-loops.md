# Chapter 11 - Loops

---

## WHILE

```python
loopIndex = 0
canCont = True

while (loopIndex >= 0 and loopIndex < 10 and canCont == True):
  print(loopIndex)
  loopIndex += 1

print("Finished")
```

## FOR EACH - List

```python
arrayObject = ["Cat", "Dog", "Rabbit", "Bear", "Mouse", "Turtle", "Squirrel"]

for animal in arrayObject:
  print(animal)
```

## FOR EACH - Character

```python
textString = "The quick Brown Fox jumps over the lazy Dog"

for currentCharacter in textString:
  if (currentCharacter != " "):
    print(currentCharacter)
```

## FOR

```python
loopIndex = -1

for loopIndex in range(10):
  print(loopIndex)
```

## Loop Range
* To loop for a set number of times, use the `range()` function.
* Returns a sequence of numbers used in `for` loops.
* Arguments: `(start, end, step)`

```python
loopIndex = -1

# Between 10 and 19
for loopIndex in range(10,20):
  print(loopIndex)
```

## Step
* It is possible to specify the increment value by adding a third argument to `range()`.
* Most of the time, this will be 1, which is the default value.
* There are times when you might want to use this.

```python
loopNumber = -1

# Every 5th number from 0 to 100
for loopNumber in range(0, 100, 5):
  print(loopNumber)

# 0, 5, 10, [...] 100
```

## Loop Passing
* Loop structures cannot be empty.
* If they need to be empty, you can use the `pass` statement.
* This is the same as with IF structures.

```python
loopIndex = -1

for loopIndex in range(0, 100):
  pass

print("Passed")
```

---

**Previous:** [10 - Conditions](./10-conditions.md)  
**Next:** [12 - Functions](./12-functions.md)

[Contents](./readme.md)