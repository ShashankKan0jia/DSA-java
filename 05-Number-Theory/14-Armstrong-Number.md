# 14. Armstrong Number

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/armstrong-numbers2727/1

**Statement:** Check if a number equals the sum of its own digits each raised to the power of the number of digits.

```java
class Solution {
    static boolean armstrongNumber(int n) {
        int original = n;
        int a = n;
        int count = 0;
        while (a != 0) {
            a = a / 10;
            count++;
        }
        int b = n;
        double sum = 0;
        while (b != 0) {
            sum = sum + Math.pow(b % 10, count);
            b = b / 10;
        }
        if (sum == original) {
            return true;
        } else {
            return false;
        }
    }
}
```
