# Pattern 1 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-1](https://static.takeuforward.org/content/ProblemSetter-dEELhBlC)

Constraints

1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to (N-1), where N is the number of rows. This loop will ensure to print each row of the pattern.

- Inner loops makes sure that N stars are printed in every line, eventually since the inner loop will run for N times, it will make sure that N stars are printed in N lines, resulting in a square of size N x N, which is the desired pattern.

- Now, print the asterisks for each column of a row, inside the inner loop.

- Move to a new line after printing each row to maintain the square structure of the pattern.

```Java
class Solution {
    // Function to print pattern1
    public void pattern1(int n) {
        
        // Outer loop will run for rows.
        for (int i = 0; i < n; i++) {
            
            // Inner loop will run for columns.
            for (int j = 0; j < n; j++) {
                System.out.print("*");
            }
            /* As soon as n stars are printed, move to the next row and give a line break. */
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 4;

        // Create an instance of the Solution class
        Solution sol = new Solution();

        sol.pattern1(N);
    }
}
```