---
title: "How to remove or Delete a File or Folder in Python"
description: "Learn how to delete a File or Folder in Python"
date: "2022-09-21T00:00:00+00:00"
draft: false
author: "dmohanty"
---

Scripting has always been a flagship feature that Python has provided to its users.

Keeping this premium feature of Python in mind, in this article , we will discuss about how to delete a file or folder from a directory / sub directory using Python.

## Method 1: Using `os.remove()`

The `os` module of python gives us full immunity to interact with the operating system and play around with the files and folders in our machine.

But the `os` methods also raise an `OSError` in case of an invalid file path or corrupted file path etc.

We can use the `os.remove()` method  delete a file from our system.

The remove method takes in two parameters, while one of them is optional.

The two parameters are:

1. `Path` : File Path
2. `dirDesc` (optional) : A file description regarding your directory / sub directory.

The `remove()` method can be invoked by, `os.remove(Path, dirDec)`.  

```python

import os     
dirName = "Test"
fileName ="file1.txt"

location = "E:\SampleFolder"


filePath = os.path.join(location, fileName)

dirPath = os.path.join(location, dirName)

os.remove(filePath)  
print("File Succesfully Removed")

os.remove(dirPath) 
print("Directory Succesfully Removed !")

"""

Output:
File Succesfully Removed

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
PermissionError: [WinError 5] Access is denied: 'E:\\SampleFolder\\Test'

"""

```

If the specified path is a directory, then the `OSError` is raised.

Thus, we can conclude that this method can’t be used for removing or deleting a directory.

But this is not a healthy approach as a good programmer.

So, being a responsible coder, we should handle all the possible errors and show some error message instead.

Let’s try to handle the `OSError` generated while trying to remove a directory.

```python
import os 
    
dirName = "Test"
location = "E:\SampleFolder"

dirPath = os.path.join(location, dirName)
try: 
    os.remove(dirPath) 
    print(" File removed successfully") 
except OSError as error: 
    print(error) 
    print("File cannot be removed")

"""
Output:

[WinError 5] Access is denied: 'E:\\SampleFolder\\Test'
File cannot be removed
"""    
```

## Method 2: Using `os.unlink()`

If you are working in UNIX operating system, then use `os.unlink()` method to delete a file in Python.

It's pretty much same as `os.remove()` method, except the it's specific to UNIX os.

```python

import os     
dirName = "Test"
fileName ="file1.txt"

location = "E:\SampleFolder"


filePath = os.path.join(location, fileName)

os.unlink(filePath)  
print("File Succesfully Removed")

```

## Method 3: Using `os.rmdir()`

We were unable to delete directories using the `remove()` method that doesn't imply that we can never remove directories ?

No, we can. It's Python and thus we always have a scope of achieving our desired result.

We can use the `rmdir()` method from the `os` module to **remove the empty directories** from our machine.

But this method can only remove the empty directories and will raise an `OSError` if the specified path is not not an empty directory.

Not specifically what we wanted but pretty similar. 

Removing empty directories are also sometimes an important use case.

```python
import os 
    
dirName = "Test"
emptyDirName = "TestClean"

location = "E:\SampleFolder"
dirPath = os.path.join(location, dirName)
emptyDirPath = os.path.join(location,emptyDirName)

os.rmdir(emptyDirPath)
print("Directory Removed")

os.rmdir(dirPath)
print("Dir Removed Successfully")

"""
Output:

Directory Removed

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
OSError: [WinError 145] The directory is not empty: 'E:\\SampleFolder\\Test'
"""
```

As mentioned above, we get an `OSError` whenever we try to **remove a non-empty directory**.

Again since, we have an error , our responsibility is to handle that user and show a nice error message for the user.

```python
import os 
    
dirName = "Test"
emptyDirName = "TestClean"

location = "E:\SampleFolder"
dirPath = os.path.join(location, dirName)

try:     
    os.rmdir(dirPath) 
    print(" File removed successfully") 
except OSError as error: 
    print(error) 
    print("File cannot be removed")

"""
Output:

[WinError 145] The directory is not empty: 'E:\\SampleFolder\\Test'
File cannot be removed
"""    
```

We will discuss about how to remove an entire directory from the machine.

## Method 4: Using `shutil.rmtree()`

Well, apart from `os` module, we can also use the `shutil` module in order to delete a complete directory from our system.

The `shutil.rmtree()` method takes in three parameters with two being optional.

1. `path`: File Path
2. `ignore_errors`: If true, errors due to failure are ignored.
3. `onerror`: if `ignore_errors` is false, then we can handle error using onerror

Let's try this method and tru to remove the directory:

```python
import shutil
import os 
    
dirName = "Test"
location = "E:\SampleFolder"

dirPath = os.path.join(location, dirName)
  
shutil.rmtree(dirPath)
print("Directory Removed !")

"""
Output:
Directory Removed !
"""

```


### Using `ignore_errors` parameter

This parameter bypasses all the weird error messages that are generated if a file is not present.


```python
import shutil
import os 
    
dirName = "Test"

location = "E:\SampleFolder"
  
dirPath = os.path.join(location, dirName)

shutil.rmtree(dirPath, ignore_errors = True)
print("File Removed ?")

"""
Output:
File Removed ?

"""

```



### Using the `onerror` parameter

The `onerror` must be assigned with a function having three parameter.

1. `function` – function which raised the exception.
2. `path` – File path that caused the exception
3. `excinfo` – exception info raised by sys.exc_info() 

```python
import shutil
import os 
    
dirName = "Test"

location = "E:\SampleFolder"
  
dirPath = os.path.join(location, dirName)
  
def Errorhandler(func, path, exc_info):
    print("Oops ! Something went Wrong")
    print(exc_info)
  
shutil.rmtree(dirPath, onerror = Errorhandler)

"""
Output:

Oops ! Something went Wrong
(<class 'FileNotFoundError'>, FileNotFoundError(2, 'The system cannot find the path specified'), <traceback object at 0x000001B4A669DE00>)
Oops ! Something went Wrong
(<class 'FileNotFoundError'>, FileNotFoundError(2, 'The system cannot find the file specified'), <traceback object at 0x000001B4A669DE00>)

"""
```

## Method 5: Using `pathlib` module

`Path` object from the Python 3.4+ `pathlib` module, contains two methods which can be used to delete a file or folder in Python. 

1. `pathlib.Path.unlink()` 
2. `pathlib.Path.rmdir()` :  

### Using `pathlib.Path.unlink()` method

Removes a file or symbolic link in Python

```python
import pathlib


fileName ="file1.txt"

location = "E:\SampleFolder"


filePath = os.path.join(location, fileName)

file = pathlib.Path(filePath)

# Call the unlink method
file.unlink()
```

### Using `pathlib.Path.rmdir()` method

Removes an empty directory in Python

```python
import pathlib

# Deleting an empty folder

empty_folder = "E:\emptyFolder"
path = pathlib.Path(empty_folder)
path.rmdir()
```


## Conclusion

In this tutorial, we discussed about the different methods to delete files and folders using Python.

First, we looked up on the different methods from the `os` module by which we were able to delete files and empty directories.

Towards the end, we discussed about the method from `shutil` module by which we could delete a complete directory.

And in the latest versions of Python we can use `pathlib` module.



