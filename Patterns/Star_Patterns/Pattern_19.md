# Pattern 19 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-19](https://static.takeuforward.org/content/ProblemSetter-T0WjHOyp)

- Constraints

    1 <= n <= 100

## Approach : 

- This pattern can be broken down into lower half and upper half. Both the halves follow the same logic, first print the asterisks then the spaces and at last the asterisks again.

- Upper half pattern: Start by initializing iniS to 0. This variable will keep track of the number of spaces between the two sets of stars in each row of the upper half pattern.

- Use an outer loop to iterate from 0 to N-1 (where N is the input parameter), representing each row of the upper half pattern.

- Print stars (*) starting from N - (the current row index) and decrementing until 1. Print spaces using another loop (for loop) that runs iniS times. iniS starts at 0 and increases by 2 with each new row. Print stars again, mirroring the first set but in reverse order.

- After completing a row give a line break, to make sure next row gets printed as well.

- Lower half pattern: Follow the same above steps to print the lower half pattern.

```Java
import java.util.*;
class Solution {
    // Function to print pattern19
    public void pattern19(int n) {
        // Print the upper half pattern
        
        // Store the initial spaces.
        int iniS = 0;
        
        for (int i = 0; i < n; i++) {
            // Printing the stars in the row.
            for (int j = 1; j <= n - i; j++) {
                System.out.print("*");
            }
            
            // Printing the spaces in the row.
            for (int j = 0; j < iniS; j++) {
                System.out.print(" ");
            }
            
            // Printing the stars in the row.
            for (int j = 1; j <= n - i; j++) {
                System.out.print("*");
            }
            
            /* The spaces increase by 2 
            every time we hit a new row. */
            iniS += 2;
            
            // Give a line break for a new row.
            System.out.println();
        }
        
        // Print the lower half pattern
        
        // Store the initial spaces.
        iniS = 2 * n - 2;
        
        for (int i = 1; i <= n; i++) {
            // Printing the stars in the row.
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            
            // Printing the spaces in the row.
            for (int j = 0; j < iniS; j++) {
                System.out.print(" ");
            }
            
            // Printing the stars in the row.
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            
            /* The spaces decrease by 2 
            every time we hit a new row. */
            iniS -= 2;
            
            // Give a line break for a new row.
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 5;
        
        // Create an instance of Solution class
        Solution sol = new Solution();
        
        sol.pattern19(N);
    }
}
```