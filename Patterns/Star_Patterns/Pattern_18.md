# Pattern 18 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-18](https://static.takeuforward.org/content/ProblemSetter-8wpcb1WC)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to N-1, where N is the number of rows. This loop will ensure to print each row of the pattern.

- The triangle has to be right-angled so, the inner loop will run for exactly current row number and the needed alphabet characters will get printed here.

- After completing a row give a line break, to make sure next row gets printed as well.

```Java
import java.util.*;
class Solution {
    // Function to print pattern18
    public void pattern18(int n) {
        // Outer loop for the number of rows.
        for (int i = 0; i < n; i++) {
            
            /* Inner loop for printing alphabets
            from A + n -1 -i (i is row no.) to
            A + n -1 ( E in this case).*/
            for(char ch = (char)(('A'+ n-1)-i); ch <= ('A'+ n-1); ch++){
                System.out.print(ch+" ");
            }

            // Move to the next line for the next row.
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 5;
        
        //Create an instance of Solution class
        Solution sol = new Solution();
        
        sol.pattern18(N);
    }
}
```