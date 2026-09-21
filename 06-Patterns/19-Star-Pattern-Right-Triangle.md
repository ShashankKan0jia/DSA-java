# 19. Star Pattern (Right Triangle)

**Statement:** Print a right-angled triangle of stars for n rows.

**Pattern:**

```
*
**
***
****
*****
```

For example, if `n = 5`, print the pattern shown above.

```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
