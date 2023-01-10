---
title: "Python iter() function syntax,usage and examples "
description: "The 'iter()' function is one of the built-in function in Python"
date: "2022-07-26T11:00:40+09:00"
draft: false
link: "iter() Built-in functions"
images: []
type: docs
menu:
  library:
    parent: "built-in-functions"
weight: 100
toc: true
---

## `iter()` function in Python

1. The `iter()` function is one of the built-in function in Python.
2. Python `iter()` is used for `Returns an iterator object`.

## `iter()` function syntax

```Python
iter(object, sentinel [optional])
```
## `iter()` function Parameters

The `iter()` method takes two parameters:
1. object - can be a list, set, tuple, etc.
2. sentinel [optional] - a special value that is used to represent the end of a sequence

## `iter()` function Return Value

The `iter()` method returns

iterator object for the given argument until the sentinel character is found
TypeError for a user-defined object that doesn't implement __iter__(), and __next__() or __getitem()__


### `iter()` function Examples:

let's go through couple of examples to understand `iter()` function in Python

## Example 1:


```Python
# list of RAINBOW COLORS
colors = ["VIOLATE", "INDIGO", "BLUE", "GREEN", "YELLOW","ORANGE","RED"]

# iter() with a RAINBOW COLOURS
colors_iter = iter(colors)


print(next(colors_iter), +1)
print(next(colors_iter), +2)
print(next(colors_iter), +3)
print(next(colors_iter), +4)
print(next(colors_iter), +5)
print(next(colors_iter), +6)
print(next(colors_iter), +7)
```
Output:

```Python
VIOLATE 1
INDIGO 2
BLUE 3
GREEN 4
YELLOW 5
ORANGE 6
RED 7
```

## Example 2:

```Python
mylist = [21, 42, 53, 74, 85]
 
# printing type
print("The list is of type : " + str(type(mylist)))
 
# converting list using iter()
mylist = iter(mylist)
 
# printing type
print("The iterator is of type : " + str(type(mylist)))
 
# using next() to print iterator values
print(next(mylist))
print(next(mylist))
print(next(mylist))
print(next(mylist))
```
output:

```Python
The list is of type : <class 'list'>
The iterator is of type : <class 'list_iterator'>
21
42
53
74
```
## Summary
In this tutorial we learnt about Python `iter()` function with simple examples