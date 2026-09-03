# Pattern 12 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-12](https://static.takeuforward.org/content/ProblemSetter-om53n9b3)

- Constraints

    1 <= n <= 100

## Approach : 

- This pattern can be divided into three parts: first print the numbers, then spaces and at last numbers again.

- Find out the numbers of spaces needs to printed in the first row and store it in a variable spaces.

- Then iterate from 1 to N to define the number of rows. Using nested for loop print the numbers as required , then in separate loop print the spaces and finally, the numbers in third loop.

- After completion of a row, decrease the number of spaces and give a line break to print next row.

```Java
class Solution {
    // Function to print pattern12
    void pattern12(int n) {
        // Initial no. of spaces in row 1.
        int spaces = 2 * (n - 1);

        // Outer loop for the number of rows.
        for (int i = 1; i <= n; i++) {
            // For printing numbers in each row
            for (int j = 1; j <= i; j++) {
                System.out.print(j);
            }

            // For printing spaces in each row
            for (int j = 1; j <= spaces; j++) {
                System.out.print(" ");
            }

            // For printing numbers in each row
            for (int j = i; j >= 1; j--) {
                System.out.print(j);
            }

            /* As soon as the numbers for each iteration
            are printed, we move to the next row and give
            a line break otherwise all numbers would get 
            printed in 1 line*/
            System.out.println();

            /* After each iteration nos. increase by 
            2, thus spaces will decrement by 2*/
            spaces -= 2;
        }
    }

    public static void main(String[] args) {
        int N = 5;

        // Create an instance of Solution class
        Solution sol = new Solution();

        sol.pattern12(N);
    }
}
```