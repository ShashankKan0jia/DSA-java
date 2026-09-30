# Maximum Average Subarray I

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/maximum-average-subarray-i/

## Problem
Given an array and integer k, find the maximum average of any contiguous subarray of size k.

## Approach
Maintain a sliding window of exactly `k` elements. Subtract the outgoing value and add the incoming value as the window moves.

## Java Solution
```java
class Solution {
    public double findMaxAverage(int[] nums, int k) {
        int windowSum = 0;
        for (int i = 0; i < k; i++) windowSum += nums[i];
        int maxSum = windowSum;
        for (int i = k; i < nums.length; i++) {
            windowSum += nums[i] - nums[i - k];
            maxSum = Math.max(maxSum, windowSum);
        }
        return (double) maxSum / k;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(1) |

---

**Practice #04** · DSA Java