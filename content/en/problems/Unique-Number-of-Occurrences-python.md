---
title: "2 ways to solve Unique Number of Occurrences Problem in Python"
description: "Given an array of integers, Write a python function to check if the number of occurrences each element in the array is unique. If they are unique return true, or else return false."
lead: ""
date: 2023-02-22T14:40:56+01:00
lastmod: 2023-02-22T14:40:56+01:00
draft: false
images: []
type: docs
author: "tribhuvan"
---

In this Tutorial we will write a `Python` program to check unique number of occurrences in a Python array. 

For example we have a Python array, and we need to check whether each element has unique number of occurrences.

There are two ways to check if the Occurrence of every element is unique in the Python array.

1. Using Using dictionary
2. Using `Counter()`

## Problem Statement

Given an array of integers `array`, Write a `python` function to check if the number of occurrences each element in the array is unique. 

If they are unique return `true`, or else return `false`.

### Input Example 1

```text
Input: array = [1,4,4,1,1,3]
Output: true
```
In the above array, the element 1 has 3 occurrences, 4 has 2 and 3 has 1. 

No two elements have the same number of occurrences so the python function should return `true`.

### Input Example 2

```text
Input: array = [1,4]
Output: false
```

The elements 1 and 4 both repeated only one time, that means same number of occurrences should return `false`

## Approach 1: Using dictionary

We will discuss two approaches to solve this problem. Initially we will solve it with using dictionary. 

The basic approach one can try is to:-

1. create another empty list and 
2. then by using two for loops count the occurrence of each and every element in the given array
3. store that count in our new list. 
4. Then convert the count list in set

After converting to list we will only be getting unique values and we will compare the length of count (which contains the count of each element) and set formed by elements of count. 

If there is a difference we will return `false`, else `true`.

You will get more insight of this point in second approach.

```python

    class Solution: 
    def uniqueOccurrences(self, arr: List[int]) -> bool: 
        d={} 
        count =[] 
        for i in arr: 
            if i in d: 
                d[i]=d.get(i)+1 
            else: 
                d[i]=1 
        for k,v in d.items(): 
            count.append(v) 
        return len(count)==len(set(count))

```


### Complexity

**Time Complexity is `O(n)`**

Where `n` is the length of the array.

**Space Complexity is `O(n)`**


## Approach 2: Using `Counter()`.

Instead of two `for` loops we can use Python built in function `Counter()` which is part of `collections`.

In this approach we will use counter container. 

`Counter` is an unordered collection where elements are stored as dict keys and their count as dict value. 

The logic here is we will store each element in counter and counter stores data as key value pair with data as key and its frequency as value. 

Eg: arr = [1,2,2,1,1,3] 

Now if we pass this array to counter 

```python
newArr = Collections.Counter(arr) 
print(newArr) 
```

It will print  

```text
Counter({1: 3, 2: 2, 3: 1}) 
```

We can see the digits and their counts are stored in this. 

Now length of counter is 3, we will also prepare a set of of values in counter which will be
`dict_values([3, 2, 1])`, it's length is also three as all three numbers are distinct so we will get true. 

Let’s look at a case where it will be `false` 

Let arr = [2,2,3,3,4,4,6,6] 

Now let’s pass it to counter 

```python
newArr = collections.Counter(arr) 
print(newArr) 
```

It will print  
```
counter({2: 2, 3: 2, 4: 2, 6: 2}) 
```

Here length of counter is 4 as there are 4 keys, but if we look clearly we will find that there are all the values 2 hence if we prepare a set of all the values of this counter we will get dict_values([2, 2, 2, 2]).

And when we convert it to `set(which stores all values uniquely)` we will get only `{2}` and the length of this set will be 1 as we have only one unique element 2. 

Hence it will return `false`. 

Let’s code this approach 


```python

    def uniqueOccurrences(self, arr: List[int]) -> bool: 
        c = collections.Counter(arr) 
        return len(c) == len(set(c.values())) 
```

### Complexity

**Time Complexity is `O(n)`**

Where `n` is the length of the array.

**Space Complexity is `O(n)`**

## Summary

In this Python tutorial, we learnt different ways to **to check unique occurrence of values in an array.**

