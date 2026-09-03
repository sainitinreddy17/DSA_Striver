# Pattern 22 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-22](https://static.takeuforward.org/content/ProblemSetter-V-DZlEjT)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to 2*N-2, where N is the number of rows. This loop will ensure to print each row of the pattern.

- Inside the outer loop, use another loop to iterate from 0 to 2*N-2. This loop controls the columns of each row.

- Assume the pattern as matrix, for each cell in the matrix, calculate how far the cell is from the matrix boundaries: top = distance to the top edge, bottom = distance to the bottom edge, right = distance to the right edge (from reverse index), left = distance to the left edge (from reverse index).

- Determine the value for each cell based on the minimum distance from the edges. This calculation ensures that cells closer to the edges have higher values, which decrease towards the center.

- After completing a row give a line break, to make sure next row gets printed as well.

```Java
import java.util.*;
class Solution {
    // Function to print pattern22
    public void pattern22(int n) {
        // Loop through all rows of the pattern
        for (int i = 0; i < 2 * n - 1; i++) {

            // Loop through all columns of the pattern
            for (int j = 0; j < 2 * n - 1; j++) {

                // Distance of current cell from all four boundaries
                int top = i;
                int left = j;
                int right = (2 * n - 2) - j;
                int bottom = (2 * n - 2) - i;

                // The minimum distance from any boundary gives the layer number
                int value = n - Math.min(Math.min(top, bottom), Math.min(left, right));

                // Print the current value
                System.out.print(value);
                if (j < 2 * n ) System.out.print(" ");
            }

            // Move to the next row
            System.out.println();
        }
    }
}

    public static void main(String[] args) {
        int N = 5;
        
        // Create an instance of Solution class
        Solution sol = new Solution();
        
        sol.pattern22(N);
    }
}
```