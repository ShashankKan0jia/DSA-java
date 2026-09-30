# Insertion Sort

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/insertion-sort/1

## Problem
Sort an array using Insertion Sort — build the sorted array one element at a time.

## Approach
Build the sorted prefix by shifting larger elements right and inserting the current key.

## Java Solution
```java
class Solution {
    public void insertionSort(int[] arr) {
        for (int i = 1; i < arr.length; i++) {
            int key = arr[i], j = i - 1;
            while (j >= 0 && arr[j] > key) { arr[j + 1] = arr[j]; j--; }
            arr[j + 1] = key;
        }
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n²) |
| Space | O(1) |

---

**Practice #17** · DSA Java