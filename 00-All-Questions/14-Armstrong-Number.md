# Armstrong Number

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/armstrong-numbers2727/1

## Problem
Check if a number equals the sum of its own digits each raised to the power of the number of digits.

## Approach
Count the digits, then calculate the sum of each digit raised to that digit count and compare it with the original number.

## Java Solution
```java
class Solution {
    static boolean armstrongNumber(int n) {
        int original = n;
        int digits = 0, temp = n;
        while (temp != 0) { digits++; temp /= 10; }
        int sum = 0;
        temp = n;
        while (temp != 0) {
            int digit = temp % 10;
            sum += (int) Math.pow(digit, digits);
            temp /= 10;
        }
        return sum == original;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(d) |
| Space | O(1) |

---

**Practice #14** · DSA Java