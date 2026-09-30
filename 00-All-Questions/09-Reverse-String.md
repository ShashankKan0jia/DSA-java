# Reverse String

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/reverse-string/

## Problem
Reverse an array of characters in-place.

## Approach
Use two pointers from opposite ends and swap characters until the pointers meet.

## Java Solution
```java
class Solution {
    public void reverseString(char[] s) {
        int left = 0, right = s.length - 1;
        while (left < right) {
            char temp = s[left]; s[left] = s[right]; s[right] = temp;
            left++; right--;
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

**Practice #09** · DSA Java