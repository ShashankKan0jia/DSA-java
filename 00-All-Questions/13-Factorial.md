# Factorial

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/factorial5739/1

## Problem
Given n, return n! (n factorial).

## Approach
Multiply the integers from 1 through n, maintaining the running factorial.

## Java Solution
```java
class Solution {
    int factorial(int n) {
        int result = 1;
        for (int i = 1; i <= n; i++) result *= i;
        return result;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(1) |

---

**Practice #13** · DSA Java