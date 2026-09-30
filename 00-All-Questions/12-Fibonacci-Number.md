# Fibonacci Number

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/fibonacci-number/

## Problem
F(0)=0, F(1)=1, and F(n)=F(n-1)+F(n-2) for n>1. Given n, return F(n).

## Approach
Use an iterative Fibonacci calculation that keeps only the previous two values, avoiding recursive recomputation.

## Java Solution
```java
class Solution {
    public int fib(int n) {
        if (n == 0) return 0;
        if (n == 1) return 1;
        int prev = 0, curr = 1;
        for (int i = 2; i <= n; i++) {
            int next = prev + curr;
            prev = curr;
            curr = next;
        }
        return curr;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) |
| Space | O(1) |

---

**Practice #12** · DSA Java