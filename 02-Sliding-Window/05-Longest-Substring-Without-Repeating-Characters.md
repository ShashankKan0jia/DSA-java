# 5. Longest Substring Without Repeating Characters

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/longest-substring-without-repeating-characters/

**Statement:** Given a string, find the length of the longest substring without repeating characters.

```java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        Set<Character> window = new HashSet<>();
        int maxSum = 0;
        int left = 0;
        for (int right = 0; right < s.length(); right++) {
            char c = s.charAt(right);

            while (window.contains(c)) {
                window.remove(s.charAt(left));
                left++;
            }
            window.add(c);
            maxSum = Math.max(maxSum, right - left + 1);
        }
        return maxSum;
    }
}
```
