---
title: "Python property() function syntax,usage and examples"
description: "The 'property()' function is one of the built-in function in Python"
date: "2022-07-26T11:00:40+09:00"
draft: false
link: "property() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `property()` function  in Python

1. The `property()` function is one of the built-in function in Python.
2. The `property()` is used for Gets, sets, `deletes a property`.
3. Python `property(`) function returns the object of the property class and it is used to create property of a class. 

## `property()` function Syntax

```Python
property(fget, fset, fdel, doc)
```
## `property()` function  Parameters 

fget() – used to get the value of attribute
fset() – used to set the value of attribute
fdel() – used to delete the attribute value
doc() – string that contains the documentation (docstring) for the attributPython property() function returns the object of the property class and it is used to create property of a class. 

## `property()` function return value

Return: Returns a property attribute from the given getter, setter and deleter.

### `property()` function Example

```Python
class Alphabet:
    def __init__(self, value):
        self._value = value
 
    # getting the values
    def getValue(self):
        print('welcome')
        return self._value
 
    # setting the values
    def setValue(self, value):
        print('Setting value to ' + value)
        self._value = value
 
    # deleting the values
    def delValue(self):
        print('Deleting value')
        del self._value
 
    value = property(getValue, setValue,
                     delValue, )
 
 
# passing the value
x = Alphabet('Pythonshiksha')
print(x.value)
 
x.value = 'Python'
 
del x.value
```
output:

```Python
welcome
Pythonshiksha
Setting value to GfG
Deleting value
```
## Summary
In this tutorial we learnt about Python `property()` function with simple examples
    