# Pattern 4 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-4](https://static.takeuforward.org/content/ProblemSetter-kbOZRims)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 1 to N, where N is the number of rows. This loop will ensure to print each row of the pattern.

- Inside this loop, run another loop from 1 to current value of the outer loop variable. It will make the number of rows and columns equal(1 column in 1st row, 2 columns in 2nd row etc).

- Now, print the current value of outer loop variable, as the row number needs to be printed in each column of the current row.

- Move to a new line after printing each row to maintain the right-angled triangle shape of the pattern.

```Java
class Solution {
    // Function to print pattern4
    public static void pattern4(int n) {
        
        // Outer loop which will loop for the rows.
        for (int i = 1; i <= n; i++) {
            
            // Inner loop which loops for the columns.
            for (int j = 1; j <= i; j++) {
                System.out.print(i);
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

        sol.pattern4(N);
    }
}
```

