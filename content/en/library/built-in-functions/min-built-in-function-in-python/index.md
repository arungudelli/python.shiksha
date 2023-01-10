---
title: "Python min() function syntax,usage and examples"
description: "The 'min()' function is one of the built-in function in Python"
date: "2022-07-08T04:30:05+09:00"
draft: false
link: "min() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `min()` function in Python

1. The `min()` function is one of the built-in function in Python. 
2. The `min()` function can return smallest number in the list or dict.
If the values are strings, an alphabetically comparison is done.

## `min()` function  syntax

```Python
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

let's go through some of examples to understand `min()` function in Python

### `min()` function Example 1:

```Python
student_marks = (71, 95, 83, 59,88,96)
x = min(student_marks) 
print("lowest marks scored:", x)
```
output:

```Python
lowest marks scored: 59
```
## `min()` function Example2 : if list is with string type

```Python
friends_list = ("kathya", "chandu", "meghana","nani")
x = min(friends_list) 
print(x)
```
output:

```Python
nani 
```
## `min()` function Example 3:

```Python
list = [1.9, 2.24,9.9,6.8,7.05]
min_value = min(list)
print(min_value)
```
output:

```Python
1.9
```
## Summary
In this tutorial we learnt about Python `min()` function with simple examples
