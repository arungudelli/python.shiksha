---
title: "Merge two sorted lists Python"
description: ""
lead: ""
date: 12 feb 2023
lastmod: 12 feb 2023
draft: false
images: []
type: docs
toc: true
---

## Problem Statement 
Merging two sorted linked lists is a common problem in computer science. Given two linked lists, each with its elements sorted in increasing order, the goal is to merge these two linked lists into a single linked list that is also sorted in increasing order. The challenge lies in merging the lists in an efficient way.

## Approach 1 : Iterative Solution 

The approach to this problem is to iterate through both linked lists and compare their elements one by one. If the element of the first linked list is smaller, append it to the result linked list, and move to the next element of the first linked list. If the element of the second linked list is smaller, append it to the result linked list, and move to the next element of the second linked list. Repeat this process until both linked lists have been fully traversed.

class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next
        
def mergeTwoLists(l1, l2):
    dummy = ListNode(0)
    cur = dummy
    while l1 and l2:
        if l1.val < l2.val:
            cur.next = l1
            l1 = l1.next
        else:
            cur.next = l2
            l2 = l2.next
        cur = cur.next
    cur.next = l1 or l2
    return dummy.next

This approach takes O(m + n) time, where m and n are the lengths of the two linked lists. The space complexity is O(1) as we are not using any extra data structures.

## Approach 2: Recursion

Another approach to solving this problem is to use recursion. The idea is to divide the problem into subproblems until it becomes simple enough to solve. In this case, we can define a helper function that takes two linked lists and returns the merged linked list. The helper function will continue to call itself with smaller and smaller linked lists until it reaches the base case where one of the linked lists is empty.

class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next
        
def mergeTwoLists(l1, l2):
    if not l1 or not l2:
        return l1 or l2
    if l1.val < l2.val:
        l1.next = mergeTwoLists(l1.next, l2)
        return l1
    else:
        l2.next = mergeTwoLists(l1, l2.next)
        return l2

This approach also takes O(m + n) time, where m and n are the lengths of the two linked lists. The space complexity is O(m + n) as the recursive call stack can be as deep as the length of the longer linked list.

## Summary

Both the iterative and recursion approaches are effective solutions to the problem of merging two sorted linked lists. The iterative solution is more space-efficient, with a time complexity of O(m + n) and a space complexity of O(1). The recursion solution also has a time complexity of O(m + n) but a higher space complexity of O(m + n) due to the call stack. The choice of approach will depend on the specific requirements and constraints of the problem, but the iterative solution is generally more efficient and easier to understand.


