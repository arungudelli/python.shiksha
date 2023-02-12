---
title: "How to get list of values from dictionary"
description: "Learn how to get list of values from dictionary"
date: "2023-02-13T04:15:05+09:00"
draft: false
author: "tribhuvan0"
---

## Introduction

In this article we will be talking about how to get the values of a dictionary in python in a separate list. 


## Methods to create a 2-D list in Python
There are various ways to handle this task. So, let’s dive into the solutions 

### Method 1: Using values() function

We can use a dictionary.values() function to get the values from the dictionary and then apply `list()` method 
to store all the values in a list. For example:- 

```python
# create a dictionary 
dict_new = {'1': 'python', '2': 'shiksha', 
         '3': 'machine', '4': 'learning'} 

# get list of values 
list(dict_new.values()) 
```

Output:
```
[‘python’,’shiksha’,’machine’,’learning’] 
```

### Method 2: Using single asterisk(*) and values() function 

We can use dictionary.values() function to get all the values of the dictionary from key:value pairs.
`*`operator is used to get only values rather than dictionary values. For example:- 

```python
# create a dictionary 
dict_new = {'1': 'python', '2': 'shiksha', 
         '3': 'machine', '4': 'learning'} 

# get list of values 
[*dict_new.values()] )
```

Output:
```
[‘python’,’shiksha’,’machine’,’learning’] 
```
### Method 3: Using a `for` loop to get values 

In this method we can take a for loop to iterate over the dictionary elements one by one and append 
all the values to a empty list one by one. For example:- 

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
### Method 4: Using list comprehension 
It is most similar to the above method. 
The only difference is that here we can perform the operations of `for` loop in one single line. 
It makes the code look cleaner. For example:- 

```python
# create a dictionary 
dict_new = {'1': 'python', '2': 'shiksha', 
        '3': 'machine', '4': 'learning'} 
        
# get list of values 
[dict_new[i] for i in dict_new] 
```
Output:
```
[‘python’,’shiksha’,’machine’,’learning’] 
```

We have learnt **four** methods of getting a list of values from dictionary

But which method is effective ?

Well , for smaller dictionaries * operator is faster, but for large dictionaries list() method works slightly better. 

## Conclusion

In this article, we briefly discussed about the various methods that can be used to create a list of dictionary values in python and we also discussed about the most **effective** method for achieving this result. 
