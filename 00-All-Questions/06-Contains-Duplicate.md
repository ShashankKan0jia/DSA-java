# 6. Contains Duplicate

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/contains-duplicate/

**Statement:** Return true if any value appears at least twice in the array, false if all elements are distinct.

```java
class Solution {
    public boolean containsDuplicate(int[] arr){Set<Integer> seen=new HashSet<>();for(int i=0;i<arr.length;i++){if(seen.contains(arr[i]))return true;else seen.add(arr[i]);}return false;}
}
```