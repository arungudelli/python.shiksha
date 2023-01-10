---
title: "Python super() function syntax, usage & example"
description: "The 'super()' function is a one of the built-in functions in python"
date: "2022-08-15T10:00:05+09:00"
draft: false
link: "python super() Built-in functions"
author: "harika"
---

## `super()` function in python:

The `super()` function is a one of the built-in functions in python.
`super()` is used for `Returns an object that represents the parent class`.

The super() function is used to give access to methods and properties of a parent or sibling class.

## `super()`syntax:
```python
super() 
```
No parameters for this function.

### Example:
```python
class stu():
    def __init__(self, rno, name, vill):
        self.Rno = rno
        self.name = name
        self.vill = vill
 
# Class freelancer inherits EMP
class Freelance(stu):
    def __init__(rno, name, vill, fn):
        super().__init__(rno, name, vill, fn)
        self.Fname = fn
 
stu_1 = Freelance(self, 20, "abcde", "hyd" , "ABCDE")

print('The RNO is:', stu_1.rno)
print('The Name is:', stu_1.name)
print('The Village is:', stu_1.vill)
print('The Father name is:', stu_1.Fname)
```
output:
```python
The RNO is: 20
The Name is: abcde
The Village: hyd
The Father name is: ABCDE
```

## Summary
In this tutorial we learnt about Python `super()` function with simple examples