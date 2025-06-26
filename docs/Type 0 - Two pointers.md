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

---

## **Easy Problems**
### Variant 1 (Single Array, Opposite Ends)
- **#125 Valid Palindrome** - Check if string reads same forwards/backwards
- **#167 Two Sum II** - Find pair that sums to target in sorted array  
- **#344 Reverse String** - Reverse character array in-place
- **#977 Squares of Sorted Array** - Return sorted squares of array elements

### Variant 2 (Two Arrays/Inputs)
- **#88 Merge Sorted Array** - Merge two sorted arrays in-place
- **#349 Intersection of Two Arrays** - Find common elements

## **Medium Problems**
### Variant 1 (Single Array, Opposite Ends)
- **#11 Container With Most Water** - Find max area between two lines
- **#15 3Sum** - Find all triplets that sum to zero
- **#16 3Sum Closest** - Find triplet closest to target sum
- **#75 Sort Colors** - Dutch flag problem (3-way partitioning)
- **#680 Valid Palindrome II** - Palindrome after deleting at most one char

### Variant 2 (Two Arrays/Inputs)  
- **#524 Longest Word in Dictionary** - Find longest word through deleting
- **#986 Interval List Intersections** - Find overlapping intervals

## **Hard Problems**
### Advanced Applications
- **#42 Trapping Rain Water** - Calculate water trapped between elevation bars
- **#407 Trapping Rain Water II** - 2D version of rain water problem
- **#76 Minimum Window Substring** - Find smallest window containing all chars
- **#4 Median of Two Sorted Arrays** - Find median efficiently

## **Study Order Recommendation**
1. **Start Easy**: Valid Palindrome → Two Sum II → Reverse String
2. **Progress Medium**: Container With Most Water → 3Sum → Sort Colors  
3. **Challenge Hard**: Trapping Rain Water → Minimum Window Substring

**Pro tip**: Master the basic templates first, then tackle problems that combine two pointers with other techniques (sliding window, binary search, etc.).
