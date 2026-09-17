# 1. Remove Duplicates from Sorted Array

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/remove-duplicates-from-sorted-array/

**Statement:** Given a sorted array, remove duplicates in-place so each unique value appears only once. Must use O(1) extra space. Return the count of unique elements.

```java
class Solution {
    public int removeDuplicates(int[] nums) {
        int slow = 0;
        for (int fast = 1; fast < nums.length; fast++) {
            if (nums[slow] != nums[fast]) {
                slow++;
                nums[slow] = nums[fast];
            }
        }
        return slow + 1;
    }
}
```
