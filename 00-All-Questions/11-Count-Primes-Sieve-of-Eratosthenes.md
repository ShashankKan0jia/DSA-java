# Count Primes (Sieve of Eratosthenes)

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/count-primes/

## Problem
Given an integer n, return the count of prime numbers strictly less than n.

## Approach
Use the Sieve of Eratosthenes. Mark multiples of each prime starting at its square, then count the remaining prime flags.

## Java Solution
```java
class Solution {
    public int countPrimes(int n) {
        if (n <= 2) return 0;
        boolean[] isPrime = new boolean[n];
        Arrays.fill(isPrime, true);
        isPrime[0] = isPrime[1] = false;
        for (int i = 2; i * i < n; i++) {
            if (isPrime[i]) {
                for (int j = i * i; j < n; j += i) isPrime[j] = false;
            }
        }
        int count = 0;
        for (boolean prime : isPrime) if (prime) count++;
        return count;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n log log n) |
| Space | O(n) |

---

**Practice #11** · DSA Java