---
title: "Python super() function syntax, usage & example"
description: "The 'super()' function is a one of the built-in functions in Python"
date: "2022-08-15T10:00:05+09:00"
draft: false
link: "Python super() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `super()` function in Python:

The `super()` function is a one of the built-in functions in Python.
`super()` is used for `Returns an object that represents the parent class`.

The super() function is used to give access to methods and properties of a parent or sibling class.

## `super()`syntax:
```Python
super() 
```
No parameters for this function.

### Example:
```Python
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
```Python
The RNO is: 20
The Name is: abcde
The Village: hyd
The Father name is: ABCDE
```

## Summary
In this tutorial we learnt about Python `super()` function with simple examples