# Chapter 12 - Functions

---

## Example

```python
def exampleFunction(subjectString, caseFlag):
  stringRes = subjectString
  stringRes = stringRes.strip()
  
  if (caseFlag > 0):
    stringRes = stringRes.upper()
  elif (caseFlag < 0):
    stringRes = stringRes.lower()
  
  return stringRes


originalString = "          The quick Brown Fox jumps over the lazy Dog          "
lowerString = exampleFunction(originalString, -1)
upperString = exampleFunction(originalString, 1)
neutralString = exampleFunction(originalString, 0)

print("---")
print(originalString)
print("")
print("Lower   : " + lowerString)
print("Upper   : " + upperString)
print("Neutral : " + neutralString)
```

## Arbitrary Arguments
* For an indefinite number of arguments, add a `\*` before the parameter name in the function definition.
	* The function will receive a tuple of arguments.
	* Individual items can be accessed accordingly.

```python
def paramsFunction(*givenArguments):
  currentArg = None
  currentType = ""
  
  print("Begin")
  print("")
  
  for currentArg in givenArguments:
    currentType = type(currentArg)
    print(currentType, currentArg)
  
  print("")
  print("End")


print("")
paramsFunction("16", 5, 24, [23, 42, 2], 19, "44", 6, 35)
```

## Default Value
Function parameters can have default values, like so:

```python
def displayCountry(countryName = "a country"):
  dispTxt = "I am from {}".format(countryName)
  print(dispTxt)


displayCountry("Australia")
displayCountry()
```

## Pass
* Similar to loop and IF structures, they cannot be empty.
* You can still use the `pass` statement to avoid errors.

```python
def emptyFunction():
  pass

emptyFunction()
print("Passed")
```

## Recursion - Theory
* Python also accepts function recursion.
	* A defined function calling itself.
* This is a common mathematical and programming concept.
* Has the benefit of calling the function in a feedback loop to achieve a result.
* One should be careful when programming recursively because it is easy to:
	* Slip into an infinite loop.
	* Use more system resources than necessary.
* When written correctly, recursion can be a very efficient and elegant approach to programming.

## Recursion - Example
* Consider this example, copied directly from [W3Schools](https://www.w3schools.com/python/python_functions.asp).
	* Use the `k` variable as data.
	* This decrements every time we recurse.
	* The recursion ends when `k` reaches Zero

```python
def tri_recursion(k):
  if(k > 0):
    result = k + tri_recursion(k - 1)
    print(result)
  else:
    result = 0
  return result

print("\n\nRecursion Example Results")
tri_recursion(6)
```

---

**Previous:** [11 - Loops](./11-loops.md)  
**Next:** [13 - Lambda](./13-lambda.md)

[Contents](./readme.md)