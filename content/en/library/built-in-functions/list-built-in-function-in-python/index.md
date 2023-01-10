---
title: "Python list() function syntax,usage examples"
description: "The `list()`function is one of the built-in function in Python"
date: "2022-07-21 T11:55:05+09:00"
draft: false
link: "list() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `list()` function in Python

1. The `list()` function is one of the built-in function in Python.
`list()` is used for `Returns a list`.
2. Lists are created using square brackets

3. Lists are one of the built-in data types in Python used to store collections of data of (Tuple, Set, and Dictionary)

## `list()` function syntax

```Python
list_name = [items]
```
## `list()` function parameters

items are ordered, changeable, and allow duplicate values.

List items are indexed, the first item has index [0], the second item has index [1] etc.

### `list()` function Examples:

let's go through couple of examples to understand `list()` function in Python

### `list()` function Example 1:

```Python
my_list = ["Pythonshiksha",29,'s',-7.5,3.9]
print(my_list)
```
output:

```Python
['Pythonshiksha', 29, 's', -7.5, 3.9]
```
like this we can store multiple data types in one variable.

### `list()` function Example 2:

```Python
fruits_list = ["apple","banana","pomegranate","guava","grapes","banana"]
print(fruits_list)
```
output:

```Python
['apple', 'banana', 'pomegranate', 'guava', 'grapes', 'banana']
```
here fruits list is created in this list banana have 2 times that means duplicate items also allows this list function in Python.

from this list we can remove,add items in to the list.

list have index values to represent items in list.
index values are useful to select any element in list to do any operations like remove,add or etc.

## Summary
In this tutorial we learnt about Python `list()` function with simple examples

