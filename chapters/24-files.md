# Chapter 24 - File Handling

---

## Introduction
* File handling is an important part of any software tool.
* Python has several functions for this.
* This is mainly achieved using the 'open' function.

## Handle Codes
| Code | Name | Description |
|---|---|---|
| r | Read | Opens a file for reading. If the file does not exist, there will be an error. (Default) |
| a | Append | Opens or creates a file for appending new text onto it. |
| w | Write | Opens or creates a file for writing. If it already exists, it will be overwritten. |
| x | Create | Creates a new file. If it already exists, there will be an error. |
| t | Text | Opens file in text mode. (Default) |
| b | Binary | Opens file in binary mode. |

## Open File
* This example opens an existing file so it can be read.
* If the file does not exist, there will be an error.

```python
exampleFile = open("example-file.txt")
print("File opened successfully")
```

## Read Contents
* This example opens an existing file, reads its contents, and displays it to the console.
* If the file does not exist, there will be an error.

```python
exampleFile = open("example-file.txt")
fileContents = exampleFile.read()
exampleFile.close()
print(fileContents)
```

## Append Content
* This example appends new text onto an existing file.
	* If the file does not exist, it will be created.
* Notice the 'a' (for append) file handling code.
* After you are done working with a file, you must release it with the `close()` function.

```python
exampleFile = open("append-file.txt", "a")
exampleFile.write("Append text onto this file")
exampleFile.close()

print("Append complete")
```

## Overwrite File
This example creates a new file, overwriting any existing content.

```python
exampleFile = open("write-file.txt", "w")
exampleFile.write("This is a new file.")
exampleFile.close()

print("Write complete")
```

## Create File
* This example creates a new file without any content.
* If the file already exists, there will be an error.

```python
exampleFile = open("create-file.txt", "x")
print("File created successfully")
```

## Delete File
* To delete files and folders, you must import the 'os' module.
* You should check if a file exists before trying to delete it.
	* If you try to delete a non-existent file, there will be an error.
* To check if a file exists, use the `os.path.exists()` function.
* To delete a file, use the `os.remove` function.

```python
import os

fileName = "delete-file.txt"
fileExists = os.path.exists(fileName)

if fileExists:
  os.remove(fileName)
  print("File deleted")
else:
  print("File does not exist")
```

## Delete Folder
* To delete folders, use the `os.rmdir()` function.
* You can only remove empty folders.

```python
import os

os.rmdir("empty-folder-path")
print("Folder deleted")
```

---

**Previous:** [23 - User Input](./23-input.md)  
**Next:**

[Contents](./readme.md)