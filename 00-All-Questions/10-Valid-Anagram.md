# Valid Anagram

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/valid-anagram/

## Problem
Given two strings, return true if the second is an anagram of the first.

## Approach
Count characters from the first string, subtract counts using the second string, and verify every final count is zero.

## Java Solution
```java
class Solution {
    public boolean isAnagram(String s, String t) {
        if (s.length() != t.length()) return false;
        Map<Character, Integer> freq = new HashMap<>();
        for (char c : s.toCharArray()) freq.put(c, freq.getOrDefault(c, 0) + 1);
        for (char c : t.toCharArray()) freq.put(c, freq.getOrDefault(c, 0) - 1);
        for (int count : freq.values()) if (count != 0) return false;
        return true;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(k) |

---

**Practice #10** · DSA Java