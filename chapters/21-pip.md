# Chapter 21 - PIP

---

## Introduction
* PIP is a package manager for Python packages and modules.
	* The same as NPM for Node JS.
* If you have Python version 3.4 or later, PIP is included by default.

## Package
* A package contains all of the files you need for a Python module.
* Modules are Python code libraries you can include in your project.

## Check PIP Install
* To check whether PIP is installed:
	* Navigate your command line to the location of Python's script directory.
	* Type the command `pip --version`
* If you do not have PIP installed, you can download it [here](https://pypi.org/project/pip/).

```
Python root path: C:\Users\[user]\AppData\Local\Programs\Python\Python36-32\Scripts
Command: pip --version
Output: pip 21.1.3 from c:\users\[user]\appdata\local\programs\python\python39\lib\site-packages\pip (python 3.9)
```

## Download Package
* For example, to download the 'camelcase' package:
	* Navigate your command line to Python's script directory.
	* Type the command `pip install camelcase`.
* Once the package is installed, it is ready to be used.
	* You can import it into your script and start using it in your code.

## Camelcase Example

```python
import camelcase as camelcaseModule

camelObj = camelcaseModule.CamelCase()
origText = "the quick brown fox jumps over the lazy dog"
prepText = camelObj.hump(origText)

print(origText)
print(prepText)
```

## Other Notes
* Refer to the [PIP website](https://pypi.org/) to find more packages.
* Use the `uninstall` command to remove a package.
* Use the `list` command to list all packages installed.

---

**Previous:** [20 - Regular Expressions](./20-regex.md)  
**Next:** [22 - Exceptions](./22-exceptions.md)

[Contents](./readme.md)