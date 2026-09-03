# Pattern 17 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-17](https://static.takeuforward.org/content/aptitude_1755981091673_1.png)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to N-1, where N is the number of rows. This loop will ensure each row of the pattern is printed.

- First, print the spaces needed before the characters in each row using an inner loop. Then, using another loop, print the alphabet characters. As observed from the pattern, the alphabet characters need to be printed incrementally up to a certain point (breakpoint) in every row, and then they need to be printed in a decreasing manner.

- After that, print the spaces that are needed after the characters for each row. Upon completion of a row, give a line break to ensure the next row is printed correctly.

```Java
import java.util.*;
class Solution {
    // Function to print pattern17
    public void pattern17(int n) {
        // Outer loop for the number of rows.
        for (int i = 0; i < n; i++) {
            
            // Printing spaces before characters.
            for (int j = 0; j < n - i - 1; j++) {
                System.out.print(" ");
            }

            // Printing characters.
            char ch = 'A';
            int breakpoint = (2 * i + 1) / 2;
            for (int j = 1; j <= 2 * i + 1; j++) {
                System.out.print(ch);
                if (j <= breakpoint)
                    ch++;
                else
                    ch--;
            }

            // Move to the next line for the next row.
            System.out.println();
        }
    }
}

class Main {
    public static void main(String[] args) {
        int N = 5;
        
        //Create an instance of Solution class
        Solution sol = new Solution();
        
        sol.pattern17(N);
    }
}
```