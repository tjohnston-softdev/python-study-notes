# Chapter 13 - Lambda

---

## Introduction
* A lambda function in Python is a small, anonymous function.
* Can take any number of arguments.
* Must only have one expression.

```python
# lambda arguments : expression
```

## Examples

```python
# Add 10 to number
addTen = lambda x : (x + 10)

# Multiply two numbers
multTwo = lambda x,y : (x * y)

# Sum three numbers
sumThree = lambda x,y,z : (x + y + z)

# Call functions
resA = addTen(35)
resB = multTwo(6,7)
resC = sumThree(1, 4, 9)

# Display results
print(resA, resB, resC)
```

## Purpose
* Lambda functions are best used as anonymous functions inside a defined function.
* Best used when it is only required for a short period of time.

---

**Previous:** [12 - Functions](./12-functions.md)  
**Next:** [14 - Classes and Objects](./14-classes_objects.md)

[Contents](./readme.md)