# Running Sum of 1D Array

## Problem
Given an array `nums`, return the running sum where  
`runningSum[i] = nums[0] + ... + nums[i]`.

---

## Approach
- Traverse from index 1 to end
- Update each element as: nums[i] += nums[i - 1]
- This accumulates prefix sums in-place

---

## Complexity
- Time: O(n)
- Space: O(1)

---

## Key Insight
Each position depends on the previous cumulative sum,  
so we build the result progressively.

---

## Example
Input: [1,2,3,4]  
Output: [1,3,6,10]

---

## Code
```python
def runningSum(nums):
    for i in range(1, len(nums)):
        nums[i] += nums[i - 1]
    return nums
