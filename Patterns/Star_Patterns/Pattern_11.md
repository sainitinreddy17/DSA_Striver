# Pattern 11 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-11](https://static.takeuforward.org/content/ProblemSetter-Q_tfusTx)

- Constraints

    1 <= n <= 100

## Approach : 

- Iterate from 1 to N using a for loop, it will basically define the number of rows needed.

- Now, if the row index is even then start from 1, else from 0. Alternatively print 0's and 1's throughout the the current row.

- Finally, print a next line at the end of a row, it ensures to print the next row as well.

```Java
class Solution {
    // Function to print pattern11
    public void pattern11(int n) {
        // First row starts by printing a single 1.
        int start = 1;

        // Outer loop for the no. of rows
        for (int i = 0; i < n; i++) {

            /* if the row index is even then 1
            is printed first in that row.*/
            if (i % 2 == 0) start = 1;

            /* if odd, then the first 0 
            will be printed in that row*/
            else start = 0;

            /* We alternatively print 1's and 0's 
            in each row by using inner for loop*/
            for (int j = 0; j <= i; j++) {
                System.out.print(start);
                System.out.print(" ");

                start = 1 - start;
            }

            /* As soon as the numbers for each 
            iteration are printed, we move to the
            next row and give a line break */
            System.out.println();
        }
    }
}

public class Main {
    public static void main(String[] args) {
        int N = 5;

        // Create an instance of Solution class
        Solution sol = new Solution();

        sol.pattern11(N);
    }
}
```