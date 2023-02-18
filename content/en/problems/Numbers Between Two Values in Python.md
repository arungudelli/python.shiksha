---
title: "Numbers Between Two Values in Python"
description: ""
lead: ""
date: 18 feb 2023
lastmod: 18 feb 2023
draft: false
images: []
type: docs
toc: true
---

## Introduction 
In Python, it is easy to create a list of numbers between two values. You can use a for loop to iterate over a range of numbers and append them to a list. In this article, we will discuss various methods to create a list with numbers between two values.

## Approach 1 : Using a for loop and range() function

The simplest method to create a list with numbers between two values is to use a for loop and the built-in range() function. The range() function creates a sequence of
numbers between the specified start and end values, with an optional step value. Here is an example code that creates a list of numbers between 1 and 10, with a step
value of 1:


numbers_list = []
for num in range(1, 11):
    numbers_list.append(num)

print(numbers_list)


Time complexity: O(n), where n is the number of integers in the range.

## Approach 2: Using list comprehension

Python provides a concise and elegant way to create a list with numbers between two values using list comprehension. List comprehension allows you to create a list in
single line of code. Here is an example code that creates a list of numbers between 1 and 10 using list comprehension:


numbers_list = [num for num in range(1, 11)]
print(numbers_list)


Time complexity: O(n), where n is the number of integers in the range.

## Approach 3: Using the numpy arrange

If you need to create a list of numbers with a large number of elements, you can use the numpy library in Python. The numpy library provides a function called arange()
that can create an array of numbers between two values. Here is an example code that creates a list of numbers between 1 and 100 using the numpy library:


import numpy as np

numbers_list = np.arange(1, 101).tolist()
print(numbers_list)


Time complexity: O(n), where n is the number of integers in the range.


## Approach 4: Using the numpy linspace

Another function in the numpy library that can create a list of numbers between two values is the linspace() function. This function creates an evenly spaced list of
numbers within a given range.


import numpy as np

def create_list(start, end):
    return np.linspace(start, end, num=end-start+1, dtype=int)


Time complexity: O(n), where n is the number of integers in the range.

## Approach 5: Using the pandas RangeIndex

The pandas library in Python provides a function called RangeIndex() that can create a range of numbers between two values, similar to the built-in range() function.
The RangeIndex() function in pandas can be used to create a list of numbers between two values. Here is an example code that creates a list of numbers between 1 and 10
using the pandas library:


import pandas as pd

numbers_list = pd.Series(pd.RangeIndex(start=1, stop=11)).tolist()
print(numbers_list)


Time complexity: O(n), where n is the number of integers in the range.

## Approach 6: Using the itertools library

Using the itertools library's count() and islice() functions
The itertools library in Python provides a count function that returns an iterator that generates an infinite sequence of numbers starting from a given value. We can 
then use the islice function to extract a finite number of elements from the iterator.


import itertools

def create_list(start, end):
    return list(itertools.islice(itertools.count(start), end-start+1))


This method has a time complexity of O(n), where n is the number of elements in the list.


## Summary

All of the approaches mentioned have a time complexity of O(n) for creating a list of numbers between two values. However, when dealing with large lists, using the
numpy library's arange() and linspace() functions are the most efficient methods as they process arrays. Overall, it is important to consider the size of the list and
the trade-off between time and space complexity when choosing the method for creating the list.
