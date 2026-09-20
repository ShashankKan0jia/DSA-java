# 2. Move Zeroes

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/move-zeroes/

**Statement:** Move all zeroes in an array to the end while keeping the relative order of non-zero elements, in-place.

```java
class Solution {
    public void moveZeroes(int[] nums) {
        int slow = 0;
        for (int fast = 0; fast < nums.length; fast++) {
            if (nums[fast] != 0) {
                int temp = nums[slow]; nums[slow] = nums[fast]; nums[fast] = temp; slow++;
            }
        }
    }
}
```