# Selection Sort

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/selection-sort/1

## Problem
Sort an array using Selection Sort by repeatedly finding the minimum element in the unsorted portion and placing it at the front.

## Approach
For each position, find the minimum in the remaining suffix and swap it into the current position.

## Java Solution
```java
class Solution {
    void selectionSort(int[] arr) {
        for (int i = 0; i < arr.length - 1; i++) {
            int minIndex = i;
            for (int j = i + 1; j < arr.length; j++) if (arr[j] < arr[minIndex]) minIndex = j;
            int temp = arr[i]; arr[i] = arr[minIndex]; arr[minIndex] = temp;
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

**Practice #18** · DSA Java