---
title: "python min() function syntax,usage and examples"
description: "The 'min()' function is one of the built-in function in python"
date: "2022-07-08T04:30:05+09:00"
draft: false
link: "min() Built-in functions"
author: "harika"
---

## `min()` function in python

1. The `min()` function is one of the built-in function in python. 
2. The `min()` function can return smallest number in the list or dict.
If the values are strings, an alphabetically comparison is done.

## `min()` function  syntax

```python
min(a1,a2,a3,a4...an)
```
            (or)
```
min(iterable)            
```
## `min()` function parameters

a1,a2..an - items present in list to do compare
iterable - one or more items in list to do compare

### `min()` function Examples:

let's go through some of examples to understand `min()` function in python

### `min()` function Example 1:

```python
student_marks = (71, 95, 83, 59,88,96)
x = min(student_marks) 
print("lowest marks scored:", x)
```
output:

```python
lowest marks scored: 59
```
## `min()` function Example2 : if list is with string type

```python
friends_list = ("kathya", "chandu", "meghana","nani")
x = min(friends_list) 
print(x)
```
output:

```python
nani 
```
## `min()` function Example 3:

```python
list = [1.9, 2.24,9.9,6.8,7.05]
min_value = min(list)
print(min_value)
```
output:

```python
1.9
```
## Summary
In this tutorial we learnt about Python `min()` function with simple examples
