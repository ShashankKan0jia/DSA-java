# First Unique Character in a String

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/first-unique-character-in-a-string/

## Problem
Find the index of the first character that appears only once in the string. Return -1 if none exists.

## Approach
Count each character first, then scan from left to right and return the first character whose frequency is one.

## Java Solution
```java
class Solution {
    public int firstUniqChar(String s) {
        Map<Character, Integer> freq = new HashMap<>();
        for (char c : s.toCharArray()) freq.put(c, freq.getOrDefault(c, 0) + 1);
        for (int i = 0; i < s.length(); i++) {
            if (freq.get(s.charAt(i)) == 1) return i;
        }
        return -1;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(k) |

---

**Practice #07** · DSA Java