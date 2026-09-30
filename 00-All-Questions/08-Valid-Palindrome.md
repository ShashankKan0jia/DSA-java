# Valid Palindrome

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/valid-palindrome/

## Problem
Check if a string reads the same forwards and backwards, ignoring case and non-alphanumeric characters.

## Approach
Use two pointers from both ends. Skip non-alphanumeric characters and compare normalized characters.

## Java Solution
```java
class Solution {
    public boolean isPalindrome(String s) {
        int left = 0, right = s.length() - 1;
        while (left < right) {
            while (left < right && !Character.isLetterOrDigit(s.charAt(left))) left++;
            while (left < right && !Character.isLetterOrDigit(s.charAt(right))) right--;
            if (Character.toLowerCase(s.charAt(left)) != Character.toLowerCase(s.charAt(right))) return false;
            left++; right--;
        }
        return true;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(1) |

---

**Practice #08** · DSA Java