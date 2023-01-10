---
title: "python callable() function syntax,usage and examples"
description: "The 'callable()' function is a one of the built-in functions in python"
date: "2022-08-18T10:10:05+09:00"
draft: false
link: "callable() Built-in functions"
author: "harika"
---

## `callable()` function in python

1. The `callable()` function is a one of the built-in functions in python.
2. The `callable()` is used for `Returns True if the specified object is callable, otherwise False`.

## `callable()` function  Syntax

```python
callable(object)
```
## `callable()` function parameter

The `callable()` method takes only one argument
an object and returns one of the two values

## `callable()`function return type
1.returns True, if the object appears to be callable.
2.returns False, if the object is not callable.

Note: There may be few cases where `callable()` returns true, but the call to object fails. But if a case returns False, calling object will never succeed

### `callable()` function Examples:

let's go through couple of examples to understand `callable()` function in python

### Example 1: 

```python
# welcome to Pythonshiksha
def num1():
  num1 = 5
def num2():
  num2 = 10
my_num = 29
print(callable(num1))
print(num2)
print(callable(my_num))
```
output:

```python
True
<function num2 at 0x2b89e74eaca0>
False
```
here num1 is called so it will  be True.
and my_num is not called so it will be False.

### Example 2:

```python
def my_num():
  a = 500

print(callable(my_num))
```
output:

```pytyhon
True
```
Try this:
You can change any number in "my_num " the output will be "True" why because "my_num" is called in this example

### Example 3:

```python
my_num= 10
print(callable(my_num))
```
output:

```python
False
```
Try this:
You can change any number in "my_num " the output will be "False" why because "my_num" is not called in this example

## Summary
In this tutorial we learnt about Python `callable()` function with simple examples.


