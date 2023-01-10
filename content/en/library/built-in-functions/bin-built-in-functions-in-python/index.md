---
title: "python bin() function syntax,usage and examples"
description: "The 'bin()' function is one of the built-in functions in python"
date: "2022-07-07 T04:30:05+09:00"
draft: false
link: "bin() Built-in functions"
author: "harika"
---
## `bin()` function in python

The `bin()` function is one of the built-in functions in python.
The `bin()` function returns the binary version of a specified integer.
The result will always start with the prefix `0b`.

## `bin()` function Syntax

```python
bin(n)
```
## `bin()` function Parameter 
n-Required. An integer

### `bin()`function Examples:
let's go through the `bin()` function examples for better understanding.

### Example 1: `bin()` for binary values

```python
# welcome to Pythonshiksha
n= bin(31)
print(n)
```
output:

```python
0b11111
```
### Example 2 : `bin()` with non integer class

```python
# welcome to Pythonshiksha
class Total_Marks:
    TELUGU = 88
    HINDI = 95
    ENGLISH = 79
    MATHS = 99
    SCIENCE = 90
    SOCIAL = 89
    
    def func():
        return TELUGU + HINDI + ENGLISH +SCIENCE+ SOCIAL
        
print('The binary equivalent of Total marks is:', bin(Total_Marks()))
```
output

```python
TypeError: 'Total_Marks' object cannot be interpreted as an integer
```
### Example 3: bin() with __index__() for Non-Integer Class

```python
# welcome to Pythonshiksha
class Total_Marks:
    TELUGU = 88
    HINDI = 95
    ENGLISH = 79
    MATHS = 99
    SCIENCE = 90
    SOCIAL = 89
    
    def __index__(self):
        return self.TELUGU + self.HINDI + self.ENGLISH +self.MATHS +self.SCIENCE+ self.SOCIAL
        
print('The binary equivalent of Total marks is:', bin(Total_Marks()))
```
output:

```python
The binary equivalent of Total marks is: 0b1000011100
```

## Summary 
In this tutorial we learnt about Python `bin()` function with simple examples.





