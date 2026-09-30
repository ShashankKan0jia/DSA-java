# Contains Duplicate

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/contains-duplicate/

## Problem
Return true if any value appears at least twice in the array, false if all elements are distinct.

## Approach
Store each value in a `HashSet`; encountering a value already in the set proves a duplicate exists.

## Java Solution
```java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        Set<Integer> seen = new HashSet<>();
        for (int value : nums) {
            if (!seen.add(value)) return true;
        }
        return false;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(n) |

---

**Practice #06** · DSA Java