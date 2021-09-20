# Chapter 14 - Classes and Objects

---

## Introduction
* Python is an object-oriented programming language.
* Almost everything in Python is some kind of object.
* Objects have their own properties and methods.
* A class can be thought of as an 'object constructor', or a blueprint.

## Example

```python
class ExampleClass:
  x = 5

localObject = ExampleClass()
print(localObject.x)
```

## Constructor
* A class constructor is the `__init__()` function.
* All classes have this function.
* It is executed automatically when a class object is initiated.
* This function can be used to:
	* Assign values to object properties. (Both specific and default)
	* Perform necessary operations during the object's creation.
* The first parameter is 'self', which refers to the object being created.

```python
class Person:
  def __init__(self, inpName, inpAge):
    self.name = inpName
    self.age = inpAge
    self.active = True

examplePerson = Person("John", 35)
print(examplePerson.name, examplePerson.age, examplePerson.active)
```

## Methods
* Objects can also contain methods.
* These are functions that belong to a particular object.

```python
class Animal:
  def __init__(self, inpName, inpNoise):
    self.name = inpName
    self.noise = inpNoise
    self.active = True
  
  def makeNoise(self):
    outputText = "{0} goes {1}".format(self.name, self.noise)
    print(outputText)


catObj = Animal("Cat", "meow")
catObj.makeNoise()
```

## Modifying Properties
Similar to dictionary (JSON) objects, you can modify and delete properties.

```python
class Person:
  def __init__(self, inpName, inpGender, inpAge):
    self.name = inpName
    self.gender = inpGender
    self.age = inpAge
    self.notNeeded = True
  
  def aboutMe(self):
    template = "My name is {0}, I am {1} years old, and my gender is {2}."
    outputText = template.format(self.name, self.age, self.gender)
    print(outputText)


examplePerson = Person("John", "Male", 35)
examplePerson.aboutMe()

examplePerson.name = "Jane"
examplePerson.gender = "Female"
del examplePerson.notNeeded

examplePerson.aboutMe()
```

## Inheritance
* Inheritance allows us to define a class that inherits all of the contents of another class.
	* Parent and Child relationship.
	* Superclass and Subclass.
* Any class can be a parent so the basic syntax is the same.

```python
class Animal:
  def __init__(self):
    self.created = True

class Cat(Animal):
  pass
```

## Child Class
* Add the `__init__()` function to the child class as you would normally.
* Child properties are set here.
* To inherit the methods and properties from the parent class, use `super().__init__()`
* If a child class method has the same name as a parent method, the child will take priority.

```python
class Person:
  def __init__(self, inpPerName, inpPerAge, inpPerGender):
    self.name = inpPerName
    self.age = inpPerAge
    self.gender = inpPerGender
  
  def introduction(self):
    template = "Hello, my name is {0}. I am {1} years old, and my gender is {2}. Nice to meet you."
    outputText = template.format(self.name, self.age, self.gender)
    print(outputText)


class Student(Person):
  def __init__(self, inpStdName, inpStdAge, inpStdGender, inpStdGradYear, inpStdMajor):
    super().__init__(inpStdName, inpStdAge, inpStdGender)
    self.gradYear = inpStdGradYear
    self.major = inpStdMajor
    self.childObject = True
  
  def studyInfo(self):
    outputText = "I studied {0} and I graduated in {1}".format(self.major, self.gradYear)
    print(outputText)



exampleObject = Student("John Smith", 35, "Male", 2021, "Software")
exampleObject.introduction()
exampleObject.studyInfo()
```

---

**Previous:** [13 - Lambda](./13-lambda.md)  
**Next:** [15 - Iterators](./15-iterators.md)

[Contents](./readme.md)