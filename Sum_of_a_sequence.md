# Instructions
Your task is to make function, which returns the sum of a sequence of integers.

The sequence is defined by 3 non-negative values: begin, end, step (inclusive).

If begin value is greater than the end, function should returns 0

---
## Solution 1
```python
def sequence_sum(begin_number, end_number, step):
   num_list = [begin_number]
   second_number = begin_number + step
   num_list.append(second_number)
   while second_number < end_number:
       i = second_number + step
       second_number = i
       num_list.append(i)

   return sum(num_list)
   
```

## Solution 2
```python
def sequence_sum(begin_number, end_number, step):
    return sum([i for i in range(begin_number, end_number+1, step)])
```