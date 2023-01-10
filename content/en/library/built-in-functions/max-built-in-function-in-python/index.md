---
title: "python max() function syntax,usage and examples"
description: "The 'max()' function is one of the built-in function in python"
date: "2022-07-08T04:30:05+09:00"
draft: false
link: "max() Built-in functions"
author: "harika"
---

## `max()` function in python

1. The `max()` function is one of the built-in function in python. 
2. The `max()` function can return highest number in the list or dict.
If the values are strings, an alphabetically comparison is done.


## `max()` function syntax

```python
max(a1,a2,a3,a4...an)
```
(or)
```python
max(iterable)            
```
##  `max()` function parameters

a1,a2..an - items present in list to do compare
iterable - one or more items in list to do compare

### `max()` function Examples:

let's go through some of examples to understand `max()` function in python

### `max()` function Example 1:  if list is integer type

```python
student_marks = (71, 95, 83, 59,88,96)
x = max(student_marks) 
print("highest marks scored:", x)
```
output:

```python
highest marks scored:96
```
### `max()` function Example 2: if list is with string type

```python
friends_list = ("kathya", "chandu", "meghana")
x = max(friends_list) 
print(x)
```
output:

```python
meghana
```
### `max()` function Example 3: if list has float values

```python
list = [1.9, 2.24,9.9,6.8,7.05]
max_value = max(list)
print(max_value)
```
output:

```python
9.9
```
## Summary
In this tutorial we learnt about Python `max()` function with simple examples
