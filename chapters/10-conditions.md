# Chapter 10 - Conditions

---

## IF Structure

```python
a = 200
b = 33

if (a > b):
  print("A is greater than B")
elif (a == b):
  print("A and B are the same")
else:
  print("B is greater than A")
```

## Short IF Statement

```python
a = 200
b = 33
print("A") if (a >= b) else print("B")
```

## Pass Statement
* IF structures cannot be empty.
* For an empty IF structure, you can use the `pass` statement to avoid errors.

```python
a = 200
b = 33

if (a > b):
  pass
elif (a == b):
  pass
else:
  pass

print("Passed")
```

---

**Previous:** [09 - Dictionaries](./09-dictionaries.md)  
**Next:** [11 - Loops](./11-loops.md)

[Contents](./readme.md)