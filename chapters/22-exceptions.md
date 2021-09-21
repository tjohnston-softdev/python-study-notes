# Chapter 22 - Exceptions

---

## Exception Handling
* When an error occurs, Python will normally stop and generate an error message.
	* These situations are called 'exceptions'.
* These exceptions can be handled safely using `try-except` structures.
	* If the `try` block raises an error, the `except` block will be executed instead.
	* Without this, the program will crash and raise a fatal error.
* Overall, these can be used to mitigate runtime errors.

## Basic Example

```python
try:
  # Use unknown variable.
  print(x)
except:
  # Error is caught safely.
  print("An exception occurred")
```

## Specific Exception Types
* You can define as many `except` blocks as you want.
	* One block for each known exception type.
	* Executing specific code for specific errors.
* For example, if you try to use an unknown variable, it will raise a `NameError` exception.

```python
try:
  # Use unknown variable.
  print(x)
except NameError:
  # Specific
  print("Name exception")
except:
  # General
  print("Other exception")
```

## Raising Exceptions
* You can choose to throw an exception if an error occurs.
* To do this, use the `raise` keyword.
* You can specify what error to raise, and what text to display.

## Raise Example - General

```python
x = -1

if (x < 0):
  raise Exception("x is negative")
```

## Raise Example - Specific

```python
x = "meow"

if not type(x) is int:
  raise TypeError("x must be a string")
```

---

**Previous:** [21 - PIP](./21-pip.md)  
**Next:** [23 - User Input](./23-input.md)

[Contents](./readme.md)