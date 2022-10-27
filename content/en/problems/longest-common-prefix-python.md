---
title: "Longest Common Prefix in Python"
description: "Different methods to find the Longest common Prefix using Python."
lead: ""
date: 2022-01-25T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
---


# Find the Longest common Prefix using Python
In this tutorial we will learn, how to find the longest common prefix using `Python`. 

## Problem Statement
Given a `list` of strings, we have to code a `Python` function to find the longest prefix that is common for all the given strings. 

Then return the prefix that is common for all strings. 

Example:
```
# Example 1
Input: ["Maths","Mat","Match"]
Output: Mat

# Example 2
Input: ["Light","Like","Lit","Listen"]
Output: Li
```
## Approach 1: Word to Word Matching

The simplest way to start with finding for the long common prefix is to compare the given strings word by word and extract the longest matching word. 

### Algorithm
* We have 2 strings, Maths and Match, the common longest common prefix that we can get from these two strings is Mat.
* We can say that finding the longest prefix word by word is similar to that of the associative property in mathematics.
```
# By Analytical
( A + B ) + C = A + B +C

# By Algorithm
Prefix(Prefix("Maths","Match"),"Mat") = Mat
```
* We go through each string one by one and check for a common prefix and after iterating through the whole collection of strings, we return the longest common prefix.

We can achieve this functionality by using two methods and, one that returns the *common prefix* between two strings and the other method that calls the first method periodically for each string inside of the collection.

```
# Utility Function that compares two strings and finds 
# the common prefix.

def findCommonPrefix(a, b):
    output = "";
    n = len(a)
    m = len(b)
 
    i = 0
    j = 0
    while i <= n - 1 and j <= m - 1: 
        if (a[i] != b[j]):
            break          
        output += a[i]
        i += 1
        j += 1
 
    return (output)
 
# Function that calls the utility function 
# periodically for each string in the collection

def getCommonPrefix (lst):
    prefix = lst[0]
    n = len(lst);
    for i in range (1, n):
        prefix = findCommonPrefix(prefix, lst[i])
    return (prefix)
```

### Complexity

**Time Complexity**: 
We are iterating through each string inside the collection and each character from each string.
Therefore, we can say that the time complexity of the above approach is `O(N1 N2)`, where N1 is the *length of the collection* and N2 is the length of the *largest prefix string* amongst them.

**Space Complexity**:
We are only storing the longest common prefix inside of the memory which is why the complexity is `O(N2)`.

## Approach 2: Character to Character Matching
In the above approach, we went on to match the strings word by word, but in this method, we will compare the strings character by character. 

### Algorithm
* We first arrange all the strings inside of a 2-D list in order for making dynamic comparison.
* Then we compare the first character of all strings and if it is same, then we add it to the longest common prefix string and then move to the second character and the method goes on. 
* We compare the strings until we find any one non-matching character in any available strings, then we stop the execution and return the result.

```
1. 
[
'L','i','g','h','t'
'L','i','t'
'L','i','k','e'
'L','i','s','t','e','n'
]

2. Output = L

3. Output = Li

# Since the third character is different in all the strings
# therefore the longest common prefix is "Li"
4. Longest Common Prefix = "Li"
```

Now that we have discussed the algorithm, let's see the method in `Python` by which we can achieve this result.

```
# Function that takes in the list pf strings as a 
# parameter and then it runs a loop until the length of the
# shortest string in the list. In a nested loop, it compares
# each character of each of the strings an
# appends it tot he output.

def getCommonPrefix(lst):
 
    shortestLength = min(len(string) for string in lst)
    
    n = len(lst)
    
    output =""
    
    for i in range(shortestLength):
        
        cur = lst[0][i]
  
        for j in range(1,n):
            if (lst[j][i] != cur):
                return output
 
        output+=cur
  
    return (output)
```
### Complexity

**Time Complexity**:
We are iterating through each character from each string in the collection.

Therefore, we can say that the time complexity of this approach is `O(N1 N2)`, where N1 is the *length of the collection* and N2 is the length of the *largest prefix string* amongst them.

**Space Complexity**:
We are only storing the longest common prefix inside of the memory which is why the complexity is `O(N2)`.

This is better than Word by Word matching approach.

As we discussed earlier, word by word matching actually traverses through each string inside the collection and then give the result which can be a drawback in case where there is a very small common prefix or no common prefix.

The first approach would traverse through the whole list of strings even though there is no common prefix but, in this approach, if there is no common prefix, we can stop the code instantaneously after the first character matching. 

## Approach 3: Sorting
One of the optimized ways to perform the desired task is by using the sorting techniques for the collection of strings.

### Algorithm
* We want to get the longest common prefix among a collection of strings. 
* In order to achieve the desired functionality, we can use the sorting methods to sort the collection.
* Since sorting in Python is performed lexicographically, the strings will be order in increasing order of the occurring alphabets.
* After that we can compare the first and last strings and find the common prefix which in turn would be the longest common prefix amongst all the strings.

```
# Method to find the longest common prefix in Python 
# using the sorting techniques.

def findLongestCommonPrefix(lst):

    n = len(lst)
    if (n == 0):
        return ""
    elif (n == 1):
        return lst[0]
    else:     
        lst.sort()
        lengthOfLast = min(len(lst[0]), len(lst[n - 1]))
        i = 0
        while (i < lengthOfLast and
               lst[0][i] == lst[n - 1][i]):
            i += 1
     
        longestPrefix = lst[0][0: i]
        return longestPrefix
```

As we can easily figure out that using the sorting method to achieve the solution is pretty easier than the other methods discussed until now.

### Complexity

**Time Complexity**:
According to the algorithm, we know that sorting in python takes `O(N2)` time, where M is the maximum no. of characters in any string.

And since we are using a while loop to compare the first and the last strings, which takes the time of `O(N1logN1)`, where N is the no. of strings inside of the list.

Then we can conclude that *this method* takes `O(N2 N1logN1)` to execute.

**Space Complexity**:
Since we are not allocating any sort of memory during the code execution, then the space complexity is `O(1)`.

## Approach 4: Divide and Conquer
In this approach we will be using the famous divide and conquer algorithm to achieve the desired solution.
 
According to this algorithm, we will divide the list of strings into 2 parts, and then we execute the same methods until the length of the strings on both the sides is reduced to one. 

After that we can return the longest common prefix between both the sides.

### Algorithm
* Dividing the strings recursively into two parts and then finding the longest common prefix of the strings so far.
* After we end the recursive method, we can merge the subarrays for the both the sides and return it to the driver function i.e., 
LCP (LCP (start to mid), LCP (mid+1, end)).

```
# Utility function that can be used to find the prefix
# between two strings 

def findCommonPrefix(a, b):
 
    output = ""
    n, m = len(a), len(b)
    i, j = 0, 0
 
    while i <= n - 1 and j <= m - 1:
     
        if a[i] != b[j]:
            break
        output += a[i]
        i, j = i + 1, j + 1
     
    return output
 
# The D&C algorithm method to find the longest common 
# prefix.

def getCommonPrefix(lst, l, h):
 
    if l == h:
        return lst[l]
 
    if h > l:
        mid = (l+h)// 2
        a = getCommonPrefix(lst,l, mid)
        b = getCommonPrefix(lst,mid+1, h)
 
        return findCommonPrefix(a, b)
```

### Complexity

**Time Complexity**:
Since we are iterating through each character of each of the string, therefore the time complexity of executing the code is `O(N1 N2)` where N1 is the number of strings inside of the list and N2 is the length of the largest string. 

**Space Complexity**:
We are only storing the longest common prefix inside of our memory and therefore the space complexity of the code is `O(N2logN1)`.


## Approach 5: Binary Search
We have already discussed about using the Sorting and the Divide and Conquer algorithm, so in this method we will discuss about the Binary search approach of solving the desired problem.

### Algorithm
* At first, we will find the shortest string. 
* Then according to the binary search algorithm, we will split the list of strings into two halves, one being from the *start to mid* and the other starting from *mid+1 to end*.
* We then check on the left half (Start - mid), if the characters are present at the corresponding indices, we then append it to the longest common prefix. 
* After that we search for the same on the right half as well i.e., mid+1 - end and check if the characters are present on the corresponding indices and for the longest common prefix as well, which would in maximum cases.

```

# Utility function to check that the provided string 
# actually contains the provided prefix i.e. the
# shortest string.

def checkForPrefix(strList, str,
                      start, end):
    for i in range(0, len(strList)):
        word = strList[i]
        for j in range(start, end + 1):
            if word[j] != str[j]:
                return False
    return True
 
# Method that returns the longest common prefix 
# amongst a list of strings.

def CommonPrefix(strlst):
    
    # Find the shortest string amongst the list of strings
    shortLen = min(len(i) for i in strlst)
    
    prefix = ""
 
    # We will perform the binary search algorithm
    # on each of the strings starting from range 
    # 0 to shortLen
    
    l, h = 0, shortLen - 1
    while l <= h:
 
        # This avoids overflow issue for 
        # high values of l and h.
        mid = int(l + (h - l) / 2)
        if checkForPrefix(strlst,strlst[0], l, mid):
             
            # Checking if all the strings inside of the list
            # contains the same prefix and if they do,
            # then append
            # it to the longest common prefix.
            
            prefix = prefix + strlst[0][l:mid + 1]
            
            l = mid + 1
        else:
            h = mid - 1
 
    return prefix
 
# Driver Code
arr = ["geeksforgeeks", "geeks",
       "geek", "geezer"]
lcp = CommonPrefix(arr)
 
if len(lcp) > 0:
    print ("The longest common prefix is " +
                                 str(lcp))
else:
    print ("There is no common prefix")
```
### Complexity

**Time Complexity**:
The time complexity of executing the code is `O(N1 N2 logN2)` where N1 is the number of strings inside of the list and N2 is the length of the largest string because of the recursive relation `T(N2)= T(N2/2) + O(N2)` 

**Space Complexity**:
We are only storing the longest common prefix inside of our memory and therefore the space complexity of the code is `O(N2)`.

## Approach 6: Trie Method
In the above approaches we looked at quite a beginner to intermediate level, and now we will be moving onto our last method which is pretty much an advanced level solution using Trie.

Trie is a Date structure in Python which is similar to that of the Binary search tree in C++.

### Algorithm
* Inserting every string onto the Trie one by one and after it is completed, we perform a walk on the Trie.
* During the walk, we go deeper inside of the tree, once we find a node having more than one child or Zero child.
* We need to check this in order to stick to the fact that the longest common prefix is a single child of its parent and is not exposed to branching.

```
ALPHABET_SIZE = 26  # In order to calculate the LCP
index = 0
class TrieNode:
	# constructor
	def __init__(self):
		self.isLeaf = False
		self.children = [None]*ALPHABET_SIZE

# Method to perform insrtion operation on the Trie.
# If it fails, we can use insert a node instead.
def insert(key, root):
	arr = root
	for level in range(len(key)):
		index = ord(key[level]) - ord('a')
		if arr.children[index] == None:
			arr.children[index] = TrieNode()
		arr = arr.children[index]
	arr.isLeaf = True

# Method that contructs the Trie
def constructTrie(arr, n, root):
	for i in range(n):
		insert(arr[i], root)

# Method that returns the number of node of the child
def countChildren(node):
	count = 0
	for i in range(ALPHABET_SIZE):
		if node.children[i] != None:
			count +=1
			
			global indexs
			indexs = i
	return count
	
# Utility function to find the Longest Common Prefix
def commonPrefix(arr, n, root):
	constructTrie(arr, n, root)
	return walkTrie(root)
	
# Method to perform walk on the Trie
# and return the longest common prefix
# by using the other utility functions.
def walkTrie(root):
	lst = root
	prefix = ""
	while(countChildren(lst) == 1 and lst.isLeaf == False):
		lst = lst.children[indexs]
		prefix += chr(97 + indexs)
	return prefix or -1
```
### Complexity

**Time Complexity**:
The time complexity for inserting all the words into the Trie is `O(N1 N2)` while to perform the walk it takes `O(N2)` time, where N1 is the number of strings inside of the list and N2 is the length of the largest string.

**Space Complexity**:
We are only storing the longest common prefix inside of our memory and therefore the space complexity of the code is `O(N2)`.

## Summary
In this article, we learnt about a very famous and easy DSA problem **Finding the longest common prefix** and we discussed with very beginner methods to very advanced methods.

After learning all the approaches and brainstorming about their time and space complexity, it's kind of difficult to give an opinion on the most optimal solution for the given problem is Character by Character Matching because it has a space complexity of `O(1)` and a Time complexity of `O(N1 N2)` which is pretty much lesser than the other methods.
