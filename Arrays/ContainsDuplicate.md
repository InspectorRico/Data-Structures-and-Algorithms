### Problem
Given an integer array nums, return true if any value appears more than once in the array, otherwise return false.

### Approach
- Use a hash set to track numbers seen so far
- Iterate through the array
- If a number already exists in the set, a duplicate is found
- Otherwise, add the number to the set

This approach avoids nested loops and ensures fast lookups.

### Time & Space Complexity
- Time: O(n)
- Space: O(n)

### Solution (Python)

def containsDuplicate(nums):
    seen = set()

    for num in nums:
        if num in seen:
            return True
        seen.add(num)

    return False
