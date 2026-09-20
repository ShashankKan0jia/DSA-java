# 10. Valid Anagram

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/valid-anagram/

**Statement:** Given two strings, return true if the second is an anagram of the first.

```java
class Solution {
    public boolean isAnagram(String s,String t){if(s.length()!=t.length())return false;Map<Character,Integer> freq=new HashMap<>();for(int i=0;i<s.length();i++){char c=s.charAt(i);freq.put(c,freq.getOrDefault(c,0)+1);}for(int i=0;i<t.length();i++){char c=t.charAt(i);freq.put(c,freq.getOrDefault(c,0)-1);}for(int count:freq.values())if(count!=0)return false;return true;}
}
```