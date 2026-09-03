# Pattern 5 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-5](https://static.takeuforward.org/content/ProblemSetter-wW-G1k5A)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to N-1, where N is the number of rows. This loop will ensure to print each row of the pattern.

- Inside this loop, run another loop from 0 to (N - current value of the outer loop variable). It will decrease the number of columns as the row value increases.

- Now, print the asterisk in the inner loop all in one line, to complete the current row.

- Move to a new line after printing each row to maintain the right-angled triangle shape of the pattern.

```Java
class Solution {
    // Function to print pattern5
    public static void pattern5(int n) {
        
        // Outer loop which will loop for the rows.
        for (int i = 0; i < n; i++) {
            
            // Inner loop which loops for the columns.
            for (int j = 0; j < n-i; j++) {
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

        sol.pattern5(N);
    }
}
```