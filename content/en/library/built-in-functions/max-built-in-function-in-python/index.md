---
title: "Python max() function syntax,usage and examples"
description: "The 'max()' function is one of the built-in function in Python"
date: "2022-07-08T04:30:05+09:00"
draft: false
link: "max() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `max()` function in Python

1. The `max()` function is one of the built-in function in Python. 
2. The `max()` function can return highest number in the list or dict.
If the values are strings, an alphabetically comparison is done.


## `max()` function syntax

```Python
max(a1,a2,a3,a4...an)
```
(or)
```Python
max(iterable)            
```
##  `max()` function parameters

a1,a2..an - items present in list to do compare
iterable - one or more items in list to do compare

### `max()` function Examples:

let's go through some of examples to understand `max()` function in Python

### `max()` function Example 1:  if list is integer type

```Python
student_marks = (71, 95, 83, 59,88,96)
x = max(student_marks) 
print("highest marks scored:", x)
```
output:

```Python
highest marks scored:96
```
### `max()` function Example 2: if list is with string type

```Python
friends_list = ("kathya", "chandu", "meghana")
x = max(friends_list) 
print(x)
```
output:

```Python
meghana
```
### `max()` function Example 3: if list has float values

```Python
list = [1.9, 2.24,9.9,6.8,7.05]
max_value = max(list)
print(max_value)
```
output:

```Python
9.9
```
## Summary
In this tutorial we learnt about Python `max()` function with simple examples
