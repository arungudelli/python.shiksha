---
title: "4 different ways to get dictionary values as a list in Python"
description: "Learn how to get list of values from dictionary"
date: "2023-02-27T00:00:00+00:00"
draft: false
author: "tribhuvan"
---

## Introduction

In this article we will be talking about 4 different ways to get dictionary values as list in python using simple examples. 

So, let’s dive into the solutions 

## Method 1: Using `list()` && `dictionary.values()` functions

We can use a `dictionary.values()` function to get the values from the dictionary and then apply `list()` method to store all the values in a list. 

The default python `dictionary.values()` returns a view of dictionary values, so we have to use `list()` method to convert them into a list.

For example:- 

```python
//Create Dictionary
dict_new = {'1': 'python', '2': 'shiksha', 
         '3': 'machine', '4': 'learning'} 

print("View of Dictionary values")
print(dict_new.values())

print("Dictionary values in List")
print(list(dict_new.values()))

```

Output:

```text
View of Dictionary values
dict_values(['python', 'shiksha', 'machine', 'learning'])
Dictionary values in List
['python', 'shiksha', 'machine', 'learning']
```

## Method 2: Using `asterisk(*)` and `dictionary.values()` function 

Instead of using `list()` method, we can use `*` operator to convert dictionary view values into a list. 

For example:- 

```python
# create a dictionary 
dict_new = {'1': 'python', '2': 'shiksha', 
         '3': 'machine', '4': 'learning'} 

# get list of values 
print([*dict_new.values()])
```

Output:
```text
['python', 'shiksha', 'machine', 'learning']
```

## Method 3: Using a `for` loop to get values 

Instead of using built in methods to get the dictionary values as a list, we can use classic `for` loop.

In this method we can take a `for` loop to iterate over the dictionary elements one by one and append all the values to a empty list one by one. 

For example:- 

```python
# create a dictionary 
dict_new = {'1': 'python', '2': 'shiksha', 
        '3': 'machine', '4': 'learning'} 

# get list of values 
value = [] 
For i in dict_new: 
   value.append(dict_new[i]) 
Print(value) 
```

Output:
```
[‘python’,’shiksha’,’machine’,’learning’] 
```
## Method 4: Using list comprehension 

It is similar to the above method. 

The only difference is that here we can perform the operations of `for` loop in one single line. 

It makes the code look cleaner. For example:- 

```python
# create a dictionary 
dict_new = {'1': 'python', '2': 'shiksha', 
        '3': 'machine', '4': 'learning'} 
        
# get list of values 
print([dict_new[i] for i in dict_new]) 
```
Output:
```
[‘python’,’shiksha’,’machine’,’learning’] 
```


We have learnt four different ways of getting a list of values from python dictionary.

But which method is effective?

Well , for smaller dictionaries (`*`) operator is faster, but for large dictionaries `list()` method works slightly better. 

## Conclusion

In this article, we briefly discussed about the various methods that can be used to get a list of dictionary values in python and we also discussed about the most **effective** method for achieving this result. 