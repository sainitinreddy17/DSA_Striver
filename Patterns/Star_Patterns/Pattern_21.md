# Pattern 21 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-21](https://static.takeuforward.org/content/ProblemSetter-N0UVhxnh)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to N-1, where N is the number of rows. This loop will ensure to print each row of the pattern.

- Inside the outer loop, use another loop to iterate from 0 to n-1. This loop controls the columns in each row. Within the inner loop, check if it's a top row, left column, bottom row, right column, if so, print a asterisk. Otherwise, print a space.

- After completing a row give a line break, to make sure next row gets printed as well.

```Java
import java.util.*;
class Solution {
    // Function to print pattern21
    public void pattern21(int n) {
        // Outer loop for the rows.
        for(int i = 0; i < n; i++){
            
            /* Inner loop for printing
            the stars at borders only.*/
            for(int j = 0; j < n; j++){
                
                if(i == 0 || j == 0 || i == n-1 || j == n-1)
                    System.out.print("*");
                else
                    System.out.print(" ");
            }
            // Move to the next row.
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 5;
        
        // Create an instance of Solution class
        Solution sol = new Solution();
        
        sol.pattern21(N);
    }
}
```