---
titlle: "python hash() function syntax,usage and examples"
description: "The 'hash()' function is a one of the built-in functions in python"
date: "2022-08-17T10:00:05+09:00"
draft: false
link: "python hash() Built-in functions"
author: "harika"
---

## `hash()` function in python

1. The `hash()` function is a one of the built-in functions in python.
2. The `hash()` is used for `Returns the hash value`of a specified object.

## `hash()` function Syntax 

```python
hash(obj)
```
## `hash()` function parameters

obj : The object which we need to convert into hash.

## `hash()` Returns value

Returns the hashed value if possible. 

### `hash()` function Examples:

let's go through couple of examples to understand `hash()` function in python

### Example 1:

```python
int_val = 10
str_val = 'pyhthonshiksha'
flt_val = 32.9
 
# Printing the hash values.
print("The integer hash value is : " + str(hash(int_val)))
print("The string hash value is : " + str(hash(str_val)))
print("The float hash value is : " + str(hash(flt_val)))
```
output:

```python
The integer hash value is : 10
The string hash value is : -635771123
The float hash value is : 214741844
```
Notice:
Integer value doesn't change in this output.

### Example 2:

```python
print(hash('python learning tutorial'))
print(hash(('python','hash','function',1)))
#hash([1,2,3,4]) #It doesn't work for lists. Will throw a TypeError
print(hash(1))
print(hash(1,2,3))
```
output:

```python
-1490055704
-386609915
1
Traceback (most recent call last):
  File "c:/Users/Vamshi/with.py", line 6, in <module>
    print(hash(1,2,3))
TypeError: hash() takes exactly one argument (3 given)
```
`hash()` can take only one argument.


## Summary
In this tutorial we learnt about Python `hash()` function with simple examples.