# 16. Bubble Sort

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/bubble-sort/1

**Statement:** Sort an array using Bubble Sort — repeatedly compare adjacent elements and swap them if they're in the wrong order.

```java
class Solution {
    public void bubbleSort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - 1 - i; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}
```
