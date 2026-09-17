# 4. Maximum Average Subarray I

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/maximum-average-subarray-i/

**Statement:** Given an array and integer k, find the maximum average of any contiguous subarray of size k.

```java
class Solution {
    public double findMaxAverage(int[] nums, int k) {
        int windowSum = 0;
        for (int i = 0; i < k; i++) {
            windowSum += nums[i];
        }
        int maxSum = windowSum;

        for (int i = k; i < nums.length; i++) {
            windowSum += nums[i] - nums[i - k];
            maxSum = Math.max(maxSum, windowSum);
        }

        return (double) maxSum / k;
    }
}
```
