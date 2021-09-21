# Chapter 15 - Iterators

---

## Introduction
* An iterator is an object which contains a countable number of values.
	* An object that can be iterated upon.
	* You can traverse through all the values.
* Examples include Lists, Tuples, Sets, and Directories.
* Strings are also contain iterators - a sequence of characters.

## Protocol
* An iterator is any object that implements the iterator protocol.
* Consists of the methods:
	* `__iter__()`
	* `__next__()`
* Consider this example copied directly from [W3Schools](https://www.w3schools.com/python/python_iterators.asp).
	* All of these objects have an `iter()` method.
	* Used to retrieve the iterator.

```python
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)

print(next(myit))
print(next(myit))
print(next(myit))
```

## Looping
* You can use a `for` loop to iterate through iterator objects.
	* Similar to looping through a list. (Array)
* When running a `for` loop, Python:
	* Creates an iterator object.
	* Executes the `next()` method for each loop iteration.

## Classes and Iterators
* To define an iterator into your class, you need to implement these methods:
	* `__iter__()` - Must return the iterator object itself.
	* `__next__()` - Must return the next value in sequence.
* To prevent infinite loops, we use the 'StopIteration' statement inside the `next()` method.

```python
class MyNumbers():
  def __iter__(self):
    self.currentValue = 1
    return self
  
  def __next__(self):
    if (self.currentValue <= 20):
      resValue = self.currentValue
      self.currentValue += 1
      return resValue
    else:
      raise StopIteration


exampleObject = MyNumbers()
exampleIterator = iter(exampleObject)

for n in exampleIterator:
  print(n)

print("")
print("Done")
```

---

**Previous:** [14 - Classes and Objects](./14-classes_objects.md)  
**Next:** [16 - Modules](./16-modules.md)

[Contents](./readme.md)