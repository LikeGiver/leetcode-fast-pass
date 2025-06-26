# Type 0 Two pointers
**Core concept**: Use two pointers to traverse data efficiently, avoiding nested loops.
## Variant 1: one input, opposite ends
**Template**
```python
def fn(arr):
    left = ans = 0
    right = len(arr) - 1

    while left < right:
        # do some logic here with left and right
        if CONDITION:
            left += 1
        else:
            right -= 1
    
    return ans
```
**When to use:** Problems involving pairs, palindromes, or finding elements that sum to a target  
**Pattern:** Start from both ends, move pointers toward center based on conditions  
**Time complexity:** O(n) instead of O(n²)  
**Examples:** Two Sum (sorted array), Valid Palindrome, Container With Most Water  
  
## Variant 2: two inputs, exhaust both
**Template**
```python
def fn(arr1, arr2):
    i = j = ans = 0

    while i < len(arr1) and j < len(arr2):
        # do some logic here
        if CONDITION:
            i += 1
        else:
            j += 1
    
    while i < len(arr1):
        # do logic
        i += 1
    
    while j < len(arr2):
        # do logic
        j += 1
    
    return ans
```
**When to use:** Merging sorted arrays, comparing sequences, finding intersections  
**Pattern:** Compare elements from both arrays, advance appropriate pointer  
**Key:** Handle remaining elements after one array is exhausted  
**Examples:** Merge Sorted Arrays, Intersection of Arrays  
