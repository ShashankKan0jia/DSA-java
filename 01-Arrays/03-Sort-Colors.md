# 3. Sort Colors (Dutch National Flag)

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/sort-colors/

**Statement:** Given an array with only 0s, 1s, and 2s, sort it in-place — 0s first, then 1s, then 2s — in a single pass.

```java
class Solution {
    public void sortColors(int[] nums) {
        int low = 0;
        int mid = 0;
        int high = nums.length - 1;

        while (mid <= high) {
            if (nums[mid] == 0) {
                int temp = nums[mid];
                nums[mid] = nums[low];
                nums[low] = temp;
                low++;
                mid++;
            } else if (nums[mid] == 1) {
                mid++;
            } else {
                int temp = nums[mid];
                nums[mid] = nums[high];
                nums[high] = temp;
                high--;
            }
        }
    }
}
```
