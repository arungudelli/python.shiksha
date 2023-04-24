---
title: "Working with Series in Python's Pandas library"
description: "How we can interact with and use Series in Python."
date: "2022-04-21T22:21:00"
draft: false
author: "JamesCBartlett"
---

In this article, we will briefly discuss **How we can interact with and use Series in Python.**.

## Overview of Pandas in Python

Pandas is a powerful data manipulation library for Python. It provides data structures to efficiently handle large datasets and perform operations on them. Pandas is commonly used to work with CSV files so is very useful to know if you have to work with excel which is a widely used software.

## Overview of Series in Pandas

A Pandas Series is a one-dimensional array-like object that can hold any data type. It is very similar to a column in a spreadsheet or a SQL table. Each element in a Series is assigned a label whcih is called an index. The index can be numeric or string-based.

In this tutorial, you will learn how to create, manipulate, and analyze Series using Pandas

## Creating Series 

In order to create a Series all you need is the data to pass in and the index is assigned automatically or you can pass in an index with the data.

```python
import pandas as pd

# Create a new Series
my_Series = pd.Series([1, 3, 5, 6])

# Creating  Series with a string index to a normal array
my_Series = pd.Series([8, 6, 1, 4], index=['a', 'b', 'c', 'd'])

# Creating  Series with an integer index to a normal array
my_Series = pd.Series([-3, 2, 9, 1], index=[3,6,4,9])

```

You can also create a Series by passing in lists, dictionarys and and ndarray.

```python
# Create a Series from a list
my_list = [10, 20, 30, 40, 50]
my_Series = pd.Series(my_list)
print(my_Series)

# Create a Series from a dictionary
my_dict = {'a': 10, 'b': 20, 'c': 30, 'd': 40, 'e': 50}
my_Series = pd.Series(my_dict)
print(my_Series)

# Create a Series from an ndarray
import numpy as np
my_array = np.array([10, 20, 30, 40, 50])
my_Series = pd.Series(my_array)
print(my_Series)
```

Output

```
0    10
1    20
2    30
3    40
4    50
dtype: int64
a    10
b    20
c    30
d    40
e    50
dtype: int64
0    10
1    20
2    30
3    40
4    50
dtype: int64
```

## Accessing the Series and its elements

You can access elements in a Series using their index labels. You can use the [] operator to access a single element or to access a number of elements.

# Accessing a single element

```python
my_Series = pd.Series([123, 456, 210,196])
print(my_Series[1])
```

Output
```
456
```

# Accessing a range of elements

```python
print(my_Series[1:3])
```

Output
```
456
210
```

## Using the `in` operator

The `in` operator evaluates the presence of an element inside the Series and returns a **boolean** value accordingly.

```python
my_Series = pd.Series([123, 456, 210,196]) 

print(456 in my_Series)
```

Output
```
True
```

Equally `in` will show if an item is not present.

```python
my_Series = pd.Series([123, 456, 210,196]) 

print(100 in my_Series)
```

Output

```
False
```

## Manipulating a Series

Just like a normal array you can manipulate a Series using a range of functions provided by pandas. Some of the basic ones are:

## Sorting a Series

```python
my_Series = pd.Series([-3, 2, 9, 1], index=['a','b','e','c'])

print(my_Series.sort_values())

print(my_Series.sort_index())
```

Output
```
a   -3
c    1
b    2
e    9
dtype: int64
a   -3
b    2
c    1
e    9
dtype: int64
```

As shown Series can be easily manipulated to organise them into an ordered fashion.

## Applying Functions to Series

You can apply a function to each element in a Series using the apply() method. This can be useful for data transformation and data cleaning.

```python
my_Series = pd.Series([-3, 2, 9, 1], index=['a','b','e','c'])

# Applying a function to each element
def add_five(x):
    return x + 5

print(my_Series.apply(add_five))
```

OUTPUT:
```
a     2
b     7
e    14
c     6
dtype: int64
```

## Filtering a Series

You can filter a Series based on a given condition using boolean indexing.

```python
my_Series = pd.Series([10, 20, 30, 40, 50])

# Filtering based on a condition
print(my_Series[my_Series > 30])
```

OUTPUT:
```
3    40
4    50
dtype: int64
```

## Aggregating a Series

You can aggregate a Series using functions such as mean(), min(), max(), and sum().

```python
# Aggregating a Series
print(my_Series.mean())
print(my_Series.min())
print(my_Series.max())
print(my_Series.sum())
```

OUTPUT:
```
30.0
10
50
150
```

## Combining multiple Series

You can combine two or more Series using the concat() method.

```python
# Combining two Series
my_Series1 = pd.Series([10, 20, 30])
my_Series2 = pd.Series([40, 50, 60])
my_Series3 = pd.concat([my_Series1, my_Series2])
print(my_Series3)
```

OUTPUT:
```
0    10
1    20
2    30
0    40
1    50
2    60
dtype: int64
```

## Handling missing values

You can handle missing values in a Series using the fillna() method.

```python
import numpy
# Handling missing values
my_Series4 = pd.Series([10, 20, np.nan, 40, 50])
print(my_Series4.fillna(0))
```

OUTPUT:
```
0    10.0
1    20.0
2     0.0
3    40.0
4     50.0
dtype: float64
```

## Conclusion

To conclude, this article has discussed a number of processing involving a Pandas Series, which are the building blocks of the pandas modules. This should give you a solid foundation to move on to working with DataFrames and exploring more of the pandas module yourself. Good luck.