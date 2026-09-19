# 17. Insertion Sort

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/insertion-sort/1

**Statement:** Sort an array using Insertion Sort — build the sorted array one element at a time, inserting each element into its correct position among the already-sorted elements before it.

```java
class Solution {
    public void insertionSort(int arr[]) {
        int n = arr.length;
        for (int i = 1; i < n; i++) {
            int key = arr[i];
            int j = i - 1;

            while (j >= 0 && arr[j] > key) {
                arr[j + 1] = arr[j];
                j--;
            }
            arr[j + 1] = key;
        }
    }
}
```
