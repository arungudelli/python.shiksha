---
title: "Two Sum Problem in Python"
description: ""
lead: ""
date: 2022-01-25T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
toc: true
---

## Problem Statement

```text
Given an unsorted integer array, find a pair with the given sum in it.
For example,
nums = [8, 7, 2, 5, 3, 1] and target = 10
here 8 + 2 =10 or 7 + 3 = 10.
You can return either of them.
```
## Examples

```python
Input:
nums = [8, 7, 2, 5, 3, 1]
target = 10
 
Output:
[0, 2]
or
[1, 4]
``` 
```python 
Input:
nums = [5, 2, 6, 8, 1, 9]
target = 12
 
Output: Pair not found
```
## solutions:

```text
1. Using Brute-Force
The "brute force solution" is the least efficient way of solving any problem. It has the worst time/space complexity–but, it is a solution. However, it is better than nothing if you are unable to come up with a more advanced approach.
For this example, we are going to use nested loops. There is an outer loop that iterates through every element and an inner loop to find two elements that sum up to k.
```

```python
def findPair(nums, target):
 
    # consider each element except the last
    for i in range(len(nums) - 1):
 
        # start from the i'th element until the last element
        for j in range(i + 1, len(nums)):
 
            # if the desired sum is found, print it
            if nums[i] + nums[j] == target:
                print([i, j])
                return
 
    # No pair with the given sum exists in the list
    print('Pair not found')
 
 
if __name__ == '__main__':
 
    nums = [8, 7, 2, 5, 3, 1]
    target = 10
 
    findPair(nums, target)
```
```text
The time complexity of the above solution is O(n2) and doesn’t require any extra space, where n is the size of the input.
```

```text
#### 2. Optimised with a Linear Solution (Using Hash Map)
Using a Hash Map, store every element of the array in the map and check if there is an element in the map/dictionary that–with the element at current index–sums up to k.
This is the Best solution with a linear runtime. At most, we are checking every element once. The downside of this solution (which your interviewer may ask) is, that it requires O(n) space, given that we potentially need to store every element in the dictionary/hash map.

So follow these steps to solve this.

-Define one map to hold the result called res
-For index i in range 0 to n – 1 (where n is the number of elements in the array)
    if target − A[i] is present in res
        return res[target − A[i]] and i as indices
    Otherwise put i into the res as res[A[i]] − = i
```


```python
# Function to find a pair in an array with a given sum using hashing
def findPair(nums, target):
 
    # create an empty dictionary
    d = {}
 
    # do for each element
    for i, e in enumerate(nums):
 
        # check if pair (e, target - e) exists
 
        # if the difference is seen before, print the pair
        if target - e in d:
            print([d.get(target - e), i])
            return
 
        # store index of the current element in the dictionary
        d[e] = i
 
    # No pair with the given sum exists in the list
    print('Pair not found')
 
 
if __name__ == '__main__':
 
    nums = [8, 7, 2, 5, 3, 1]
    target = 10
 
    findPair(nums, target)
```
```text
The time complexity of the above solution is O(n) and requires O(n) extra space, where n is the size of the input.
```
