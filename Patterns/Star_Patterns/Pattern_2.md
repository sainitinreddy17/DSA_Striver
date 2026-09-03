# Pattern 2 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-2](https://static.takeuforward.org/content/ProblemSetter-EOD0D_P8)

- Constraints

1 <= n <= 100

## Approach : 

- First, run a loop for N times(0 to N-1). This loop will ensure to print each row of the pattern.

- Inside the outer loop, run another loop for current value of the outer loop variable. It will basically ensure that the total columns is equal to the current row.

- Within the inner loop, print an asterisk (*) without moving to a new line. This keeps all asterisks for a single row on the same line.

- After the inner loop completes, move to a new line to start printing the next row.

```Java
class Solution {
    // Function to print pattern2
    public static void pattern2(int n) {
        
        // Outer loop which will loop for the rows.
        for (int i = 0; i < n; i++) {
            
            // Inner loop which loops for the columns.
            for (int j = 0; j <= i; j++) {
                System.out.print("*");
            }
            /* As soon as stars for each iteration are printed,
             move to the next row and give a line break */
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 5;

        // Create an instance of Solution class
        Solution sol = new Solution();

        sol.pattern2(N);
    }
}
```