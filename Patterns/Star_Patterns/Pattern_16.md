# Pattern 16 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-16](https://static.takeuforward.org/content/ProblemSetter-W7228zcJ)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to N-1, where N is the number of rows. This loop will ensure to print each row of the pattern. Initialize a variable to store the alphabet that needs to be printed in each row, depending upon the row numbers.

- The inner loop will run for row times and print the alphabets as required.

- After completing a row give a line break, to make sure next row gets printed as well.

```Java
class Solution {
    // Function to print pattern16
    void pattern16(int n) {
        // Outer loop for the number of rows.
        for (int i = 0; i < n; i++) {
            
            // Defining character for each row.
            char ch = (char) ('A' + i);
            for (int j = 0; j <= i; j++) {
                
                /* same char is to be printed
                i times in that row.*/
                System.out.print(ch);
            }
            /* As soon as the letters for each 
            iteration are printed, we move to the
            next row and give a line break otherwise
            all letters would get printed in 1 line. */
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 5;

        // Create an instance of Solution class
        Solution sol = new Solution();

        sol.pattern16(N);
    }
}
```