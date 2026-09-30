# Star Pattern (Right Triangle)

**Type:** Pattern / Java fundamentals

## Problem
Print a right-angled triangle of stars for n rows.

## Expected Pattern
```text
*
**
***
****
*****
```

## Approach
Use nested loops: row i prints exactly i stars.

## Java Solution
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) System.out.print("*");
            System.out.println();
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

**Practice #19** · DSA Java