# 18. Selection Sort

**Platform:** GeeksforGeeks  
**Link:** https://www.geeksforgeeks.org/problems/selection-sort/1

**Statement:** Sort an array using Selection Sort — repeatedly find the minimum element from the unsorted portion and swap it into its correct position at the front.

```java
class Solution {
    void selectionSort(int[] arr){int n=arr.length;for(int i=0;i<n-1;i++){int minIndex=i;for(int j=i+1;j<n;j++)if(arr[j]<arr[minIndex])minIndex=j;int temp=arr[i];arr[i]=arr[minIndex];arr[minIndex]=temp;}}
}
```