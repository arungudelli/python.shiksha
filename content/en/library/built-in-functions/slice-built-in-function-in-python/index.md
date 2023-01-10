---
title: "python slice() function syntax,usage and examples"
description: "The 'slice()' function is a one of the built-in functions in python"
date: "2022-08-15T07:19:05+09:00"
draft: false
link: "slice() Built-in functions"
author: "harika"
---

## slice() function in python:
The `slice()` function is a one of the built-in functions in python.
`slice()` is used for `Returns a slice object`.

Based on the supplied range, the slice() method returns a section of an iterable as an object of the slice class.

It can be used with sequence objects that implement the __getitem__() and __len__() methods, such as strings, lists, tuples, sets, bytes, range objects, or custom class objects. 

## `slice()` Syntax:
```python
slice(stop)
slice(start, stop, step)
```
## `slice()` Parameters:

    start: (Optional) Starting index where the slicing of the iterable starts. Default value is none.
    stop: Ending index where the slicing should end.
    step: (Optional) An integer to increment starting index. Defaults to None.

## `slice()`Return Value:

Returns an object of the slice class.

### Example:
```python
nums = [1,2,3,4,5,6,7,8,9,10]

skip_portion = slice(0,10,3)
print(nums[skip_portion])

odd_portion = slice(0, 10, 2)
print(nums[odd_portion])

even_portion = slice(1, 10, 2)
print(nums[even_portion])
```
output:
```python
[1, 4, 7, 10]
[1, 3, 5, 7, 9]
[2, 4, 6, 8, 10]
```
here only selected slice portion will get output fom the numbers.
like this index values(positive and negative)technique also helps to slice the portion of user choice.

## Summary
In this tutorial we learnt about Python `slice()` function with simple examples

