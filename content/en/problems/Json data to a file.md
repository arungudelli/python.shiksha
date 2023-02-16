---
title: "how to write Json data to a file"
description: ""
lead: ""
date: 2022-01-25T14:40:56+01:00
lastmod: 2022-01-25T14:40:56+01:00
draft: false
images: []
type: docs
toc: true
---
## Overview Of Json

`JSON` (Javascript Object Notation) is a lightweight,text-based format for storing and exchanging data that is commonly used in web `APIs` and configuration files.

Regardless of the approach you choose, it's important to be familiar with the structure of `JSON` data and how it maps to python objects.Understanding the `JSON` data structure and tools available for working with it can help you effieciently manipulate and work with `JSON` files in python.

How `Json` data looks:

```python
data={'foo': 'bar',
 'key': 'value',
 'the answer': 42}
```

## Different methods to write Json data to a file

Let's start exploring the various python approaches to **write json data to a file.**

## Uing the `built-in` `json` modules.

The json moduke is included in python's library,which means it doesn't require any additional installation or setup,Here's an example.

```python
import json

#parse JSON data from a file
with open('data.json','r') as f:
     data=json.load(f)

#Encode Python objects into JSON data
data={'name':'jhon','age':30}
json_data=json.dumps(data)

#print JSON data
print(json.dumps(data,indent=4))
```

## Using the `pandas` library:

Before usong this approach,You have to install the `pandas` library if you haven't install it.

Use simple english to explain the soultion.

Then write python code

Add Time Complexity and Space complexity (if applicable)

## Summary

Give summary of different approaches and optimal soultion
