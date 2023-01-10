---
title: "zip() function in Python"
description: "The 'zip()' function is one of the Built in functions in python"
date: "2022-03-12T03:45:00+09:00"
draft: false
link: "zip() built-in function"
author: "harika"
---

## `zip()` in python
1. The `zip()` function is one of the Built in functions in python"
2. In Python `zip()` is a in-built function, it connects multiple lists in to one simple list. 


## How to use `zip()` in Python list

We have two lists with names and cities, from which we can create a single list with `zip()` function.

### Example

```python
names =["saanvi","vamshi","santhosh"]
city =["hyderabad","mumbai","secundrabad"]
zipped=list(zip(names,city))
print(zipped)
```
output:

```python
[(‘saanvi’,’Hyderabad’),(‘Vamshi’,’mumbai’),(‘santhosh’ ‘secundrabad’)]
```
In names list we have three items, and cities have three items.

Names are paired with city names, and we have a list. 

## How to use zip() in set:

### Example : A set is an unordered structure that produces unique values.

```python
names =["saanvi","vamshi","santhosh","saanvi"]
city =["hyderabad","mumbai","secundrabad","hyderabad"]
zipped=set(zip(names,city))
print(zipped)
```
output:

```python
[(‘saanvi’,’Hyderabad’),(‘Vamshi’,’mumbai’),(‘santhosh’ ‘secundrabad’)]
```
Names have four items, and cities have four items. 

Names are paired with city names, and we have a list, but In this list saanvi and Hyderabad values are repeated in the list,so those variables are not displayed here, why because a set have unique values.

To overcome this problem zip() is used with for loop.

### Example:

```python
names =["saanvi","vamshi","santhosh","saanvi"]
city =["hyderabad","mumbai","secundrabad","hyderabad"]
zipped = zip(names,city)
for (a,b) in zipped:
 print(a,b)
```
output:
```python
saanvi hyderabad
Vamshi Mumbai
Santhosh secundrabad
Saanvi hyderabad
``` 
## How to use zip() in dictionaries:
In this dictionaries also zip() is used same in list in
python.

### Example:
```python
names =["saanvi","vamshi","santhosh"]
city =["hyderabad","mumbai","secundrabad"]
zipped=dict(zip(names,city))
print(zipped)
```
output:
```python
[(‘saanvi’,’Hyderabad’),(‘Vamshi’,’mumbai’),(‘santhosh’ ‘secundrabad’)]
```

## Summary
In this tutorial we learnt about Python `zip()` function with simple examples