# 15. GCD and LCM

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/lcm-and-gcd4516/1

**Statement:** Given two numbers, find their GCD (Greatest Common Divisor) and LCM (Least Common Multiple).

```java
class Solution {
    public static int[] lcmAndGcd(int a, int b) {
        int m = a;
        int n = b;
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        int lcm = (m * n) / a;
        return new int[]{lcm, a};
    }
}
```
