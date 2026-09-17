# 12. Fibonacci Number

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/fibonacci-number/

**Statement:** F(0)=0, F(1)=1, F(n)=F(n-1)+F(n-2) for n>1. Given n, return F(n).

```java
class Solution {
    public int fib(int n) {
        if (n == 0) {
            return 0;
        }
        if (n == 1) {
            return 1;
        }
        int a = 1;
        int b = 0;
        for (int i = 2; i <= n; i++) {
            int current = a + b;
            b = a;
            a = current;
        }
        return a;
    }
}
```
