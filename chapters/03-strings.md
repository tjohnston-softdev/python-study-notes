# Chapter 03 - Strings

---

## Array of Characters
* Like many other programming languages, a Python string is an array of bytes that represent unicode characters.
	* Python does not have a character type in itself.
	* A 'character' is simply a string with a length of 1
* Square brackets can be used to access string characters.

```python
fullString = "I am a string"
singleChar = fullString[2]

# Prints 'a'
print(singleChar)
```

## String Looping
Since strings are arrays, you can loop through individual characters.

```python
for x in "meow":
  print(x)
```

## Length
Retrieved using the `len()` function.

```python
baseString = "Hello World"
stringLength = len(baseString)
outputText = ""

outputText += "'baseString' has "
outputText += str(stringLength)
outputText += " characters."

print(outputText)
```

## Includes
* To check for a certain substring, use the `in` keyword.
* For the opposite, use `not in`
* Can be used in IF statements and other condition checks.

```python
baseString = "Cats go meow"

if "meow" in baseString:
  print("Yes, Cats do meow")

if "woof" not in baseString:
  print("No, Cats do not woof")

print("Finished")
```

## Slicing
* You can return a range of characters from a string using the slice syntax.
	* In other words, a substring.
* To do this, specify the start and end index separated by colon. `[x:y]`
* The 'start' character is included, but not the 'end' character.
* Leave out the start index to slice up to a certain point from the beginning of the string/
* Leave out the end index to slice from a certain point to the end of the string.

```python
baseString = "The quick Brown Fox jumps over the lazy Dog"

startSub = baseString[:20]
generalSub = baseString[20:30]
endSub = baseString[31:]

print(startSub)
print(generalSub)
print(endSub)
```

## Negative Slicing
Use negative index numbers to slice from the end of the string.

```python
baseString = "Hello World"
startInd = -5
endInd = -2
subString = baseString[startInd:endInd]
print(subString)
```

## General Methods
* `upper()` returns the string in uppercase.
* `lower()` returns the string in lowercase.
* `strip()` removes leading whitespace from the beginning and end.
	* Same as `trim()` from JavaScript
* `replace()` searches for a substring and replaces it with another.
* `split()` returns a list of substrings between the given separator.

```python
baseString = "     The quick Brown Fox jumps over the lazy Dog     "
trimStr = baseString.strip()

upperStr = trimStr.upper()
lowerStr = trimStr.lower()
catStr = trimStr.replace("Dog", "Cat")
wordsList = trimStr.split(" ")

print(upperStr)
print(lowerStr)
print(catStr)
print(wordsList)
```

## Formatting
The `format()` method takes passed arguments, formats them, and writes them into placeholders specified throughout the string.

```python
itemCount = 7
unitPrice = 4.56
itemID = 123

baseStr = "I want to buy {0} of the item #{2} at ${1} each."
prepStr = baseStr.format(itemCount, unitPrice, itemID)

print(prepStr)
```

## Decimal Places
* As well as including passed arguments, you can also specify how they are formatted in the final text.
* This example formats and displays a price number to two decimal places.

```python
itemNo = 123
price = 4.56789
grpMin = 8

template = "Item #{0} costs ${1:.2f} each when you buy at least {2} of them in bulk."
finalText = template.format(itemNo, price, grpMin)

print(finalText)
```

## Escape Quotes
The escape character `\` allows you to use quotation marks where they would not normally be allowed.

```python
strTxt = "I'm \"shipping up\" to Boston."
print(strTxt)
```

## Escape Characters Table
| Code | Description |
|---|---|
| `\'` | Single quote |
| `\"` | Double quote |
| `\\` | Backslash |
| `\n` | New line |
| `\r` | Return |
| `\t` | Tab |
| `\b` | Backspace |
| `\f` | Form feed |
| `\ooo` | Octal value |
| `\xhh` | Hex value |


---

**Previous:** [02 - Syntax](./02-syntax.md)  
**Next:** [04 - Booleans](./04-booleans.md)

[Contents](./readme.md)