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

two_sum(A=[5,7, 2], S=9) 

<!-- Naive Solution - Two Nested Loops, O(n²) -->
def two_sum(A, S):
	pairs = []
	for i in range(len(A)):
		for j in range(i+1, len(A)):
			if A[i] + A[j] == S:
				pairs.append((i, j))

	return pairs
  
<!-- Using a Hash Map - O(n) {for optimal solution} -->
def two_sum(A, S):
	index_dict = build_index_dict(A)

	pairs = []
	for i in range(len(A)):
		C = S - A[i]
		if C in index_dict:
			j = index_dict[C]
			if j > i:
				pairs.append((i, j))

	return pairs
