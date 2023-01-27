# Instructions
___
Given an array of integers, find the one that appears an odd number of times.

There will always be only one integer that appears an odd number of times.

---
## Solution 1
```python
def find_it(seq):
    for elem in seq:
        if seq.count(elem) % 2 != 0:
            return elem
```
## Solution 2
```python
def find_it(seq):
    dict = {}
    for i in seq:
        if i not in dict:
            dict[i] = 1
        else:
            dict[i] = dict.get(i) + 1
    for k, v in dict.items():
        if v % 2 != 0:
            return k
