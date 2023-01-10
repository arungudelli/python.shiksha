---
title: "python sorted() function syntax,usage and examples"
description: "The 'sorted()' function is a one of the built-in functions in python"
date: "2022-08-15T08:10:05+09:00"
draft: false
link: "sorted() Built-in functions"
author: "harika"
---

## `sorted()` function in python:
The `sorted()` function is a one of the built-in functions in python.
`sorted()` is used for`Returns a sorted list`.

## Syntax:
```python
sorted(iterable, key, reverse)
```
where,
iterable: The iterable to be arranged in ascending or descending order.
key: (Optional) A function that serves as a key for the sort comparison.
reverse: (Optional) If true, sorts in descending order.

## `sorted()`Return Value:

Returns a list object with sorted items.

### Example:
```python
nums = [62,21,35,83,]
asc_nums = sorted(nums)
dsc_nums = sorted(nums, reverse = True)
print("Ascending Numbers: ", asc_nums)
print("Descending Numbers: ", dsc_nums)
```
output:
```python
Ascending Numbers:  [21, 35, 62, 83, 144]
Descending Numbers:  [144, 83, 62, 35, 21]
```
## Summary
In this tutorial we learnt about Python `sorted()` function with simple examples