# Move Zeroes

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/move-zeroes/

## Problem
Move all zeroes in an array to the end while keeping the relative order of non-zero elements, in-place.

## Approach
Use a write pointer for the next non-zero position. Scan the array once and swap every non-zero value into that position.

## Java Solution
```java
class Solution {
    public void moveZeroes(int[] nums) {
        int slow = 0;
        for (int fast = 0; fast < nums.length; fast++) {
            if (nums[fast] != 0) {
                int temp = nums[slow];
                nums[slow] = nums[fast];
                nums[fast] = temp;
                slow++;
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

**Practice #02** · DSA Java