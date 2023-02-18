---
title: "Append integer to begining od list in Python"
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

Appending an integer to the beginning of a list is a common operation in Python. There are many ways to perform this operation, 
with varying levels of efficiency. In this article,  We will analyze the different methods and will also analyse the time 
complexity of different method and provide a summary of the most efficient approaches.


## Approach 1 : Iterative Solution 

The insert() function in Python is used to insert an element at a particular index in a list. In this case, we can insert the 
integer at the beginning of the list by passing the index 0. Here's an example:


my_list = [2, 3, 4]
my_list.insert(0, 1)
print(my_list) # [1, 2, 3, 4]


Time complexity: O(n)

## Approach 2: Using list concatenation

In Python, you can concatenate two lists using the '+' operator. We can create a list with the integer we want to add and the 
original list, and then concatenate them to get the final list. Here's an example:


my_list = [2, 3, 4]
my_list = [1] + my_list
print(my_list) # [1, 2, 3, 4]


Time complexity: O(n)


## Approach 3: Using the list.insert() method with a slice

Another way to use the insert() function is to pass a slice that covers the entire list, which will insert the integer at the 
beginning. Here's an example:


my_list = [2, 3, 4]
my_list[0:0] = [1]
print(my_list) # [1, 2, 3, 4]


Time complexity: O(n)

## Summary

Appending an integer to the beginning of a list in Python can be achieved using the insert() function or list concatenation method.
The insert() function has a time complexity of O(n), as it needs to shift all the elements to make room for the new element. The  
list concatenation method has the same time complexity of O(n). However, the third method of using the list.insert() method with a
slice also has the same time complexity of O(n) but it has the advantage of being more concise and readable than the other two 
methods.

