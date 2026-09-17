# 9. Reverse String

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/reverse-string/

**Statement:** Reverse an array of characters in-place.

```java
class Solution {
    public void reverseString(char[] s) {
        int left = 0;
        int right = s.length - 1;
        while (left < right) {
            char temp = s[left];
            s[left] = s[right];
            s[right] = temp;
            left++;
            right--;
        }
    }
}
```
