# Sort Colors

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/sort-colors/

## Problem
Given an array with only 0s, 1s, and 2s, sort it in-place — 0s first, then 1s, then 2s — in a single pass.

## Approach
Use the Dutch National Flag algorithm with `low`, `mid`, and `high` pointers to partition 0s, 1s, and 2s in one pass.

## Java Solution
```java
class Solution {
    public void sortColors(int[] nums) {
        int low = 0, mid = 0, high = nums.length - 1;
        while (mid <= high) {
            if (nums[mid] == 0) {
                int temp = nums[mid]; nums[mid] = nums[low]; nums[low] = temp;
                low++; mid++;
            } else if (nums[mid] == 1) {
                mid++;
            } else {
                int temp = nums[mid]; nums[mid] = nums[high]; nums[high] = temp;
                high--;
            }
        }
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(1) |

---

**Practice #03** · DSA Java