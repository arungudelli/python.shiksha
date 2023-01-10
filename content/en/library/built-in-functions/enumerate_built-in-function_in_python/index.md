---
title: "python enumerate() function syntax,usage and examples"
description: "The 'enumerate()' function is a one of the built in functions in python
"
date: "2022-06-28T11:25:05+09:00"
draft: false
link: "enumerate() built-in function"
author: "harika"
---

## `enumerate()` function in python

1.The `enumerate()` function is a one of the built in functions in python.

In python `enumerate()` function can acts as a counter, it will count the items present in list or tuple.

## `enumerate()` function Syntax

```python
enumerate(iterable, start=0)
```
## `enumerate()` function Parameters

Iterable: any object that supports iteration
Start: the index value from which the counter is to be started, by default it is 0

### `enumerate()` function Examples:

let's go through couple of examples to understand `enumerate()` function in python

### Example 1:

```python
students =['saanvi','kathya','hasya']
print(list(enumerate(students)))
```
output:
```
[(0,saanvi),(1,katya),(2,hasya)]
```
Like this the counter starts from 0 and ends when all the list of variables executes

### Example 2:

```python
# initializing numbers in to the list
numbers =[5,6,10,8,89,0,34,77]
print(list(enumerate(numbers)))
```
output:

```python
[(0, 5), (1, 6), (2, 10), (3, 8), (4, 89), (5, 0), (6, 34), (7, 77)]
```
Like this the counter starts from 0 and ends when all the list of variables executes

## Summary
In this tutorial we learnt about Python `enumerate()` function with simple examples.
