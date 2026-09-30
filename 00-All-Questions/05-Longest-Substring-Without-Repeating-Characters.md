# Longest Substring Without Repeating Characters

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/longest-substring-without-repeating-characters/

## Problem
Given a string, find the length of the longest substring without repeating characters.

## Approach
Maintain a sliding window containing unique characters. Move `left` forward until the repeated character is removed.

## Java Solution
```java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        Set<Character> window = new HashSet<>();
        int maxLength = 0, left = 0;
        for (int right = 0; right < s.length(); right++) {
            char c = s.charAt(right);
            while (window.contains(c)) {
                window.remove(s.charAt(left++));
            }
            window.add(c);
            maxLength = Math.max(maxLength, right - left + 1);
        }
        return maxLength;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(k) |

---

**Practice #05** · DSA Java