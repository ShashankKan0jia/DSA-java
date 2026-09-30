# GCD and LCM

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/lcm-and-gcd4516/1

## Problem
Given two numbers, find their GCD (Greatest Common Divisor) and LCM (Least Common Multiple).

## Approach
Apply Euclid's algorithm for GCD. Compute LCM from `(a × b) / GCD`.

## Java Solution
```java
class Solution {
    public static int[] lcmAndGcd(int a, int b) {
        int originalA = a, originalB = b;
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        int gcd = a;
        int lcm = (originalA / gcd) * originalB;
        return new int[]{lcm, gcd};
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(log(min(a,b))) |
| Space | O(1) |

---

**Practice #15** · DSA Java