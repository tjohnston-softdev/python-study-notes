# Chapter 02 - Syntax

---

## Hello World
The 'print' function is used to display text to console.

```python
print("Hello World")
```

## Indentation
* Refers to spaces at the beginning of the line.
* While indentation is only for readability in most languages, it is very important in Python.
* Used to indicate blocks of code.
* If the indentation is skipped, there will be bugs or errors.
* The number of spaces used for indentation has to be at least one.
	* Relative to parent block.
* Each line in a given block has to have the same indentation.

```python
# Valid
if 5 > 2:
  print("5 is greater than 2")
```

```python
# Invalid
if 5 > 2:
print("The indentation is missing")
```

## Comments
Marked with the # character.

```python
# This is an in-line comment.


print("Actual code goes here")


#     ----------------------------------------------------
#
#                      This is a block comment.
#
#     ----------------------------------------------------

print("Done")
```

## Variables
* No specific command for declaring variables.
* Created the moment you first assign to a name.
* Python is weakly-typed.
	* Variables are not declared as a particular type.
	* The type depends on the value.
	* Can be changed on-the-fly.
* In short, it is similar to JavaScript but without the var command.

```python
x = 5;             # Number
y = "Hello"        # String

print(x)
print(y)
```

## Variable Naming
* Must start with a letter or underscore.
* Cannot start with a number.
* Can only contain alphabet, numbers, and underscores
* Names are case-sensitive.


## Assign Multiple Variables
* Python allows you to assign multiple variables in one line.
	* Make sure the number of variables matches the number of values.
	* Otherwise, there will be an error.


```python
x, y, z = "Cat", "Dog", "Rabbit"

print(x)
print(y)
print(z)
```

## Global Variables
* Variables created outside of a function can be used globally.
	* If you create a variable with the same name inside a function, it will be local and take precedence inside that scope.
	* Maybe you shouldn't do that.

```python
x = "meow"

def exampleFunction():
  print("Cats go " + x)

exampleFunction()
```

## Function Globals
* To create or change a global variable inside a function, use the global keyword.
* Declaring and assigning are on separate lines.


```python
x = "meow"

def exampleFunction():
  global x
  x = "woof"
  print("Cats go " + x)

exampleFunction()
```

## Get Data Type
The data type of a value can be retrieved using the 'type' function.

```python
baseValue = "Hello World"
valType = type(baseValue)
print(valType)
```

## Data Types
| Name | Set | Cast |
|---|---|---|
| str | "Hello World" | str("Hello World") |
| int | 20 | int(20) |
| float | 20.5 | float(20.5) |
| complex | 123j | complex(123j) |
| list | ["Cat", "Dog", "Rabbit"] | list(("Cat", "Dog", "Rabbit")) |
| tuple | ("Cat", "Dog", "Rabbit") | tuple(("Cat", "Dog", "Rabbit")) |
| range | range(6) | range(6) |
| dict | {"name" : "John", "age" : 36} | dict(name="john", age=36) |
| set | {"Cat", "Dog", "Rabbit"} | set(("Cat", "Dog", "Rabbit")) |
| frozenset | frozenset({"Cat", "Dog", "Rabbit"}) | frozenset(("Cat", "Dog", "Rabbit")) |
| bool | True | bool("X") |
| bytes | b"Meow" | bytes(4) |
| bytearray | bytearray(5) | bytearray(5) |
| memoryview | memoryview(bytes(5)) | memoryview(bytes(5)) |

## Complex Numbers
* Written with 'j' as the imaginary part
* Cannot be converted into other number types.


```python
x = 3+5j
y = 123j
z = -123j

print(x)
print(y)
print(z)
```

---

**Previous:** [01 - Introduction](./01-introduction.md)
**Next:** [03 - Strings](./03-strings.md)

[Contents](./readme.md)