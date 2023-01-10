---
title: "python getattr() function syntax,usage and examples"
description: "The 'getattr()' function is a one of the built-in functions in python"
date: "2022-08-22T12:00:05+09:00"
draft: false
link: "python getattr() built-in functions"
author: "harika"
---

## `getattr()` function in python

1. The `getattr()` function is a one of the built-in functions in python.
2. The `getattr()`is used for `Returns the value of the specified attribute (property or method)`.

3. The `getattr()` method returns the value of the attribute of an object. If the named attribute does not exist, default is returned if provided, otherwise AttributeError is raised.

## `getattr()` function Syntax

```python
getattr(object, name, default)
```
## `getattr()` function Parameters

    object: An object of the class whose attribute value needs to be returned.
    name: The string name of the attribute.
    default. (Optional) A value to be returned if the attribute is not found.

## `getattr()` function Return Value

    Returns value of the attribute of the given object.
    Returns the specified default value if attribute not found.
    If the default value not specified, then throws AttributeError.

### `getattr()` function Examples:

let's go through couple of examples to understand `getattr()` function in python

###  Example 1:

```python
class employee:
    name = 'aaaa'
    age = 18
    
emp = employee() # creating object

print('employee name is ', getattr(emp, 'name'))

emp.name = 'bbbb' # updating value
print('employee name changed to ', getattr(emp, 'name'))
```
output:

```python
employee name is  aaaa
employee name changed to  bbbb
```
###  `getattr()` Example 2:

```python
class employee:
    name = 'aaaa'
    age = 18
    
emp = employee() # creating object

print('employee name is ', getattr(emp, 'gender'))
```
output:

```python
print('employee name is ', getattr(emp, 'gender'))
AttributeError: 'employee' object has no attribute 'gender'
```
in this gender attribute is not created so it gives error

## Summary
In this tutorial we learnt about Python `getattr()` function with simple examples.