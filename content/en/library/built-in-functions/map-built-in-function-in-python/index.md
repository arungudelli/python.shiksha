---
title: "python map() function syntax,usage and examples"
description: "The 'map()' function is a one of the built-in functions in python"
date: "2022-08-18T03:05:05+09:00"
draft: false
link: "map() Built-in functions"
author: "harika"
---

## `map()` function in python

1. The `map()` function is a one of the built-in functions in python.
2. The `map()` is used for	`Returns the specified iterator with the specified function applied to each item`.

For each item in an iterable, the map() function calls a predefined function.
The object is passed as a parameter to the function. 

# `map()` function Syntax 

```python
map(fun, iter)
```
## `map()` function parameters

`map()` function can take two parameters
1. fun : It is a function to which map passes each element of given iterable.
2. iter : It is a iterable which is to be mapped.

NOTE : You can pass one or more iterable to the `map()` function.

## `map()` function Returns

Returns a list of the results after applying the given function  
to each item of a given iterable (list, tuple etc.) 

NOTE : The returned value from map() (map object) then can be passed to functions like list() (to create a list), set() (to create a set) .

### `map()` function Examples:

let's go through couple of examples to understand `map()` function in python

### `map()` function Example 1:

```python
def mylist(a, b):
  return a + b
x = map(mylist, ('apple', 'banana', 'cherry'), ('orange', 'lemon', 'pineapple'))
print(x)

#convert the map into a list, for readability:
print(list(x))
```
output:

```python
['appleorange', 'bananalemon', 'cherrypineapple']
```
### `map()` function Example 2:

```python
num1 = [8, 9, 6]
num2 = [9, 6, 8]

result = map(lambda n1, n2: n1+n2, num1, num2)

print(list(result))
```
output:

```python
[17,15,14]
```
## Summary
In this tutorial we learnt about Python `map()` function with simple examples


