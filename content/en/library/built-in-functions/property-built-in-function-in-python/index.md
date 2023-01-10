---
title: "python property() function syntax,usage and examples"
description: "The 'property()' function is one of the built-in function in python"
date: "2022-07-26T11:00:40+09:00"
draft: false
link: "property() Built-in functions"
author: "harika"
---

## `property()` function  in python

1. The `property()` function is one of the built-in function in python.
2. The `property()` is used for Gets, sets, `deletes a property`.
3. Python `property(`) function returns the object of the property class and it is used to create property of a class. 

## `property()` function Syntax

```python
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

```python
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
x = Alphabet('pythonshiksha')
print(x.value)
 
x.value = 'python'
 
del x.value
```
output:

```python
welcome
pythonshiksha
Setting value to GfG
Deleting value
```
## Summary
In this tutorial we learnt about Python `property()` function with simple examples
    