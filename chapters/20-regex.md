# Chapter 20 - Regular Expressions

---

## Introduction
* A Regular Expression is a sequence of characters that form a search pattern.
* Can be used to check if a string contains a specific search pattern.
* Python has a built-in module used for regular expressions.
	* This module is called 're'

```python
import re as regex
print("Imported")
```

## Example
* This example checks if a string starts with 'The' and ends with 'Spain'.
* Copied directly from [W3Schools](https://www.w3schools.com/python/python_regex.asp).

```python
import re

#Check if the string starts with "The" and ends with "Spain":

txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)

if x:
  print("YES! We have a match!")
else:
  print("No match")

```

## RegEx Functions
| Function | Description |
|---|---|
| `findall(pattern, string)` | Returns a list containing all matches of the target pattern in the source string. |
| `search(pattern, string)` | Searches the source text for the target pattern, returning a match object if any results are found. |
| `split(pattern, string)` | Returns a list of substrings with the source string split on target pattern matches. |
| `sub(pattern, replace, string, max)` | Replaces up to 'max' number of 'pattern' matches in 'string' with 'replace'. |

## Meta Characters
| Character | Description | Example |
|---|---|---|
| \[\] | Set of characters | \[a-z\], \[q, w, e, r, t, y\] |
| \ | Signals a special sequence, or escapes special characters. | \d |
| ^ | String starts with | ^Hello |
| $ | String ends with | World!$ |
| \* | Zero or more occurrences (Optional) | text\* |
| + | One or more occurrences (Required) | text+ |
| {x} | Exactly x number of occurrences. | text{3} |
| \| | Either/Or | Yes|No |
| () | Capturing group | (syntax) |

## Special Sequences
| Character | Description | Example |
|---|---|---|
| \A | String starts with | \AHello |
| \b | Characters are at the beginning or end of a word. (Note: The "r" at the beginning signifies a raw string.) | r"\bain" |
| \B | Characters that are in a word, but not the beginning or end. | r"\Bain" |
| \d | Digit | 0-9 |
| \D | Not a digit |  |
| \s | Whitespace | Spaces, tabs, etc |
| \S | Not whitespace |  |
| \w | Word character | A-Z, a-z, 0-9, underscore |
| \W | Not a word character |  |
| \Z | String ends with | Spain\Z |

## Sets
| Set | Description |
|---|---|
| \[arn\] | Any of these characters. |
| \[a-z\] | Any characters in the range |
| \[^arn\] | Any characters except for these. |
| \[0-5\]\[0-9\] | Matches any number from 00 - 59 |
| \[a-zA-Z\] | Alphabet character (Case insensitive) |
| \[+\] | Although this is a special character, escaping is not required when in a set. |

## Find All
* The `findall()` function returns a list containing all matches of a target pattern in the source string.
* Matches are listed in the order they are found.
* If there are no matches found, an empty list will be returned.

```python
import re

sourceText = "The rain in Spain"
matchList = re.findall("ain", sourceText)
print(matchList)
```

## Search
* The `search()` function searches the string for a match, returning a Match object.
	* If there are multiple matches, only the first is returned.
	* If there are no matches, return `None`.

```python
import re

sourceText = "Hello World!"
matchObj = re.search("\s", sourceText)
spacePos = matchObj.start()
displayText = "Whitespace location: {}".format(spacePos)
print(displayText)
```

## Split
* The `split()` function returns a list of substrings from the source string, split at pattern match.
* Parameters:
	* Target pattern.
	* Source string.
	* Maximum split count.
* When using the maximum split count, the rest of the string will be used as a single element.

```python
import re

sourceText = "The quick Brown Fox jumps over the lazy Dog."
splitList = re.split("\s", sourceText, 5)
print(splitList)
```

## Replace
* The `sub()` function searches a target pattern and replaces it with text.
* Parameters:
	* Target pattern.
	* Replace text.
	* Source string.
	* Maximum replacement count.

```python
import re

origText = "The quick Brown Fox jumps over the lazy Dog."
prepText = re.sub("\s", "-", origText, 5)
print(prepText)
```

## Match Object
* Contains information about the RegEx search and the results.
* Returned from the 'search()' function.
	* Remember, if there is no match, `None` will be returned instead.
* This object has properties and methods used to retrieve information about the search.
	* `.span()` - Tuple containing the start/end positions of the match.
	* `.string` - String passed into the search function.
	* `.group()` - Returns the part of the string where there was a match.

---

**Previous:** [19 - JSON](./19-json.md)  
**Next:** [21 - PIP](./21-pip.md)

[Contents](./readme.md)