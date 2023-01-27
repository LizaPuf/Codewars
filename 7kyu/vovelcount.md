# Instructions
___
Return the number (count) of vowels in the given string.

We will consider a, e, i, o, u as vowels for this Kata (but not y).

The input string will only consist of lower case letters and/or spaces.


## Solution 1
```python
def get_count(sentence):
    all_vowels = ['a', 'e', 'i', 'o', 'u']
    vowelsc_count = 0
    for i in sentence:
        if i in all_vowels:
            vowelsc_count += 1
    return vowelsc_count