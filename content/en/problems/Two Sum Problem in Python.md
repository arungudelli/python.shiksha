---
title: "Two sum problem in python"
description: "How to solve two sum problem"
lead: ""
date: 2023-02-15T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
weight: 2
---

The problem is that you are given an array of integers and an integer sum, return indexes of the two numbers
such that the sum of two numbers is equal to sum.

**Assumptions**
1. Each input would have exactly one solution,
2. You should not use the same element twice.
3. Return the indexes in any order.

```
//Example

Input: nums = [3,2,4], target = 6
Output: [1,2]

```

## Approach 1: Brute force

This approach is based on using two nested `for` loops. We will take two pointers in the loops say i and j, the first pointer (say i) will iterate 
over the outer loop and the second pointer (say j) will iterate over inner loop, for every value of i it will iterate from location i+1 to length of 
the array (say n) in the inner loop and will check at each step that is sum of both the numbers that are at i and j indices
of the array equals to the target sum or not. 

For example :           
Let’s suppose our array, nums = [2,0,3,1,6] and target = 5 
Then, outer for loop will fix the value of first pointer (i) at location 0. So the value of i = 0.
And the inner for loop will decide location of second pointer(j) at location i+1. So, initially j = i+1 = 0+1 = 1.
 
Now, for i = 0 and j = 1, sum = nums[0] + nums[1]  = 2+0 = 2.
Since sum is not equal to target sum. So, inner loop will increment the value of j again.
And now for i = 0 , j = 2, sum = nums[0] + nums[2] = 2+3 = 5 = target.
Hence, i = 0 and j =2 is returned.


```python

    class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums)):
            for j in range(i + 1, len(nums)):
                if nums[i] + nums[j] == target:
                    return [i, j]
        return []

```

### Complexity

**Time Complexity is `O(m*n)`**

Where `n` is the length of the array.

**Space Complexity is `O(1)`**


## Approach 2: Using dictionary Hash Table

In this approach, initially an empty dictionary is created. 
                                        List = { }
Then a `for` loop is iterated over the array. The first element at the beginning of the list is taken by the for loop, 
and we check that if our second number (second number = target – first number) is present in the dictionary or not.

For example, if we are given an equation 5 + a = 8, in order to find `a` we do `a = 8 – 5 = 3`, same approach we are following here. 
We have target given and we start from first element of list. Now target – first number = second number. 
So at whichever index if that second number exists we will return that.

Let’s suppose our array, nums = [2,0,3,1,6] and target = 5
Initially, i = 0, so for first number nums[i] = 2, if target – nums[i] = 5-2 = 3 is present or not.
If the second number = target – first number is not present in the dictionary then add the first number along with index.
So,      for i=0,      List = { 2 : 0}
         for i=1,     List = { 2 : 0, 0:1}
         for i=2,     second = target – nums[2] = 5-3 = 2 which is present in List.
So, return the index i and index of second number from the dictionary.


```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        
        d = {}
        for i, j in enumerate(nums):
            r = target - j
            if r in d: return [d[r], i]
            d[j] = i
	
}
```
### Complexity

**Time Complexity is `O(n)`**

Where `n` is the length of the array.

**Space Complexity is `O(n)`**


## Summary

In this Python tutorial, we learnt different ways to **Solve two sum problem in python.**

Prefer using Hashtable method as it is more optimised approach.
