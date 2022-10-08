---
title: "Merge two sorted linked lists in python"
description: "ou are given the heads of two sorted linked lists list1 and list2.

Merge the two lists in a one sorted list. The list should be made by splicing together the nodes of the first two lists.

Return the head of the merged linked list."
lead: ""
date: 2022-10-8T15:33:56+01:00
lastmod: 
draft: false
images: []
type: docs
toc: true
---

[Problem Statement] (https://github.com/arungudelli/python.shiksha/issues/50)
You are given the heads of two sorted linked lists list1 and list2.

Merge the two lists in a one sorted list. The list should be made by splicing together the nodes of the first two lists.

Return the head of the merged linked list.
Examples:
1)For example if the first linked list a is 5->10->15 and the other linked list b is 2->3->20, then the function should return a pointer to the head node of the merged list 2->3->5->10->15->20.
2)For example: if L1 = 1 -> 3 -> 10 and L2 = 5 -> 6 -> 9 then your program should output the linked list 
1 -> 3 -> 5 -> 6 -> 9 -> 10.

Approach 1: Using temporary or dummy nodes
This method here uses a temporary dummy node as the start of the result list. 
Using this approach we can append new nodes at the end easily. 
The pointer tail of this dummy node always points to the end of the list that is the answer to this problem. 
This dummy is temporary and it is allocated in the stack. Using loop, 
we remove nodes one by one from the given lists and append it to the resulting list in required order.  


```python
def mergeLists(A_head, B_head):
  
    dummy = Node(0)
    tail = dummy
    while True:
        if A_head is None:
            tail.next = B_head
            break
        if B_head is None:
            tail.next = A_head
            break
        if A_head.data <= B_head.data:
            tail.next = A_head
            A_head = A_head.next
        else:
            tail.next = B_head
            B_head = B_head.next
  
        tail = tail.next
  
    return dummy.next  
```
Approch 2: Using recursion.
In this case the recursive approach is much more cleaner than the previous.
In this the base cases are the ones where either of the given lists becomes empty.


```python
ef mergeLists(A_head, B_head):
  
    temp = None
    if A_head is None:
        return B_head
    if B_head is None:
        return A_head
    if A_head.data <= B_head.data:
        temp = A_head
        temp.next = mergeLists(A_head.next, B_head)    
    else:
        temp = B_head
        temp.next = mergeLists(A_head, B_head.next)
    return temp
```
Time Complexity:  Since we are traversing through the two lists fully.
So, the time complexity is O(m+n) where m and n are the lengths of the two lists to be merged. 


Approach 3: Reversing the lists
In this method we will first reverse both the lists and then after comparing each elements of the 
lists seeing for the larger one we will add this element at the beginning of our final merged list.


This method is mere a different way of doing this problem than the 1st method.
    
    
Summary:
Here in this section we learned about different ways of merging two pre sorted linked lists 
into one along with the basic alogorithm and the code implementations in python with the intuition
of what the time complexity will look like in each case.
