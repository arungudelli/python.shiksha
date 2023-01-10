---
title: "python tuple() function syntax,usage and examples"
description: "The `tuple()`function is a one of the built in functions in python"
date: "2022-07-01T03:30:05+09:00"
draft: false
link: "tuple() built-in function "
author: "harika"
---

## `tuple()` function in python:

1. The `tuple()` function is a one of the built in functions in python.
2. It is used to create a tuple.
3. Tuple is a immutable sequence type.

## `tuple()` function syntax

```python
tuple(itertor)
```

## `tuple()` function Parameters

iterable​ (optional) - an iterable (list, range, etc.) or an iterator object.

If the iterable is not passed to tuple(), the function returns an empty tuple.

### `tuple()` function Examples:

let's go through couple of examples to understand `tuple()` function in python


### `tuple()` function Example 1: To create empty tuple:

```python
t1 = tuple()
print('t1 =', t1)
```
output:

```python
t1 = ()
```

### `tuple()` function Example 2: To create a tuple from a list:

```python
t2 = tuple([22,35,7,9.2])
print('t2 =', t2)
```
output:

```python
t2 = 22,35,7,9.2
```
### `tuple()` function Example 3: To create a tuple from a string

```python
t1 = tuple('Python')
print('t1 =',t1)
```
output:

```python
t1 = ('P', 'y', 't', 'h', 'o', 'n')
```
### `tuple()` function Example 4: To create a tuple from a dictionary:

```python
t1 = tuple({1: 'one', 2: 'two' , 3:'three'})
print('t1 =',t1)
```
output:

```python
t1 = (1,2,3)
```

## Summary
In this tutorial we learnt about Python `tuple()` function with simple examples






