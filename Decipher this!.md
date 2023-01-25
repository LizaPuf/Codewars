# Instructions
the second and the last letter is switched (e.g. Hello becomes Holle)
the first letter is replaced by its character code (e.g. H becomes 72)
Note: there are no special characters used, only letters and spaces
---
## Solution 1
```python
import re


def decipher_single_word(word):
    pattern = r'(\d+)(\D+)'
    results = re.match(pattern, word)
    change = []
    from_number_to_word = chr(int(results.group(1)))
    change.append(from_number_to_word)
    str = results.group(2)
    list_str = list(str)
    list_str[0], list_str[-1] = list_str[-1], list_str[0]
    new_list = change + list_str
    return ''.join(new_list)


def decipher_this(string):
    words = string.split()
    result = []
    for word in words:
        result.append(decipher_single_word(word))
    return ' '.join(result)