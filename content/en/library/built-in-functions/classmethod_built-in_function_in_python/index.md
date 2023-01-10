---
title: "python classmethod()function syntax,usage and examples"
description: "The 'classmethod()' function is one of the built-in functions in python"
date: "2022-07-07 T004:30:05+09:00"
draft: true
link: "classmethod() Built-in functions"
author: "harika"
---


## `classmethod()` function in python

1. The `classmethod()` function is one of the built-in functions in python.
2. The `classmethod()` is used for `Converts a method into a class method`

##  `classmethod()` function syntax

```python
classmethod(function)
@classmethod
   def fun(cls, arg1, arg2, ...)
```

##  `classmethod()` function parameter

Parameter :This function accepts the function name as a parameter
    fun: the function that needs to be converted into a class method

##  `classmethod()` function return type

Return Type:This function returns the converted class method.

###   `classmethod()` function Examples:

let's go through couple of examples to understand `classmethod()` function in python

### Example 1:

```python
class School:
    # class variable
    name = 'XYZ School'

    def school_name(cls):
        print('School Name is :', cls.name)

# create class method
School.school_name = classmethod(School.school_name)

# call class method
School.school_name()
```
output:

```python
School Name is : XYZ School
```
## Example 2:

```python
class vegetable:
    name = 'vegetables'

    def printName(cls):
            print('The name is:', cls.name)

vegetable.printAge = classmethod(vegetable.printName)
vegetable.printAge()
```
output:

```python
The name is: vegetables
```

## classmethod vs staticmethod

1. A class method, like a static method, does not require the instantiation of an object. 

2. A static method has no knowledge of the class or instance.
You might also use a function call. 

3. a class method gets the class when the method is called. It knows about's the classes attributes and methods.


## Summary
In this tutorial we learnt about Python `classmethod()` function with simple examples.

