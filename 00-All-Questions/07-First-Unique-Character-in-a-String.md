# 7. First Unique Character in a String

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/first-unique-character-in-a-string/

**Statement:** Find the index of the first character that appears only once in the string. Return -1 if none exists.

```java
class Solution {
    public int firstUniqChar(String s){Map<Character,Integer> freq=new HashMap<>();for(int i=0;i<s.length();i++){char c=s.charAt(i);freq.put(c,freq.getOrDefault(c,0)+1);}for(int i=0;i<s.length();i++){if(freq.get(s.charAt(i))==1)return i;}return -1;}
}
```