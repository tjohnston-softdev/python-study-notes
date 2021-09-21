# Chapter 16 - Modules

---

## Introduction
* A module is a library of code.
* Contains properties and functions you may want to include when writing a program.
* To require a file similar to in Node JS, use the `import` statement.
	* eg. `import moduleName`

## Usage Syntax

`[moduleName].[itemName]`

## Alias
* When importing a module, you can include an alias.
	* If the module is a variable, the alias is the name of that variable.
* To do this, use the `as` keyword.
	* eg. `import moduleName as aliasName`

## Example
Copied directly from [W3Schools](https://www.w3schools.com/python/python_modules.asp).

**Parent**
```python
person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```

**Child**
```python
import mymodule as mx

a = mx.person1["age"]
print(a)
```

## Platform Module
* The 'platform' module is one of Python's built-in modules that can be imported whenever you need it.
* Displays system-related information.
* For example, the 'system' method retrieves the local Operating System.

```python
import platform

os = platform.system()
print(os)
```

## List Module Properties
* To retrieve all functions and properties in an imported module, use the `dir()` function.
	* This function is built-in.
* Can be used on all modules, including the ones you create yourself.

```python
import platform

varList = dir(platform)

for item in varList:
  print(item)
```

## Import From
* You can choose to only import particular variables from a module instead of the whole thing.
* This is done by using the `from` keyword.
	* `from moduleName import varName`
* Example copied directly from [W3Schools](https://www.w3schools.com/python/python_modules.asp).

**Parent**
```python
def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```

**Child**
```python
from mymodule import person1

print(person1["age"])
```

---

**Previous:** [15 - Iterators](./15-iterators.md)  
**Next:** [17 - Datetime Module](./17-datetime.md)

[Contents](./readme.md)