# Pattern 8 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-8](https://static.takeuforward.org/content/ProblemSetter-8ShPenE-)

- Constraints

    1 <= n <= 100

## Approach : 

- Iterate from 0 to N-1 using a loop, where N is the number of rows. This loop will ensure to print each row of the pattern.

- Now, run another loop from 0 to the current value of outer loop variable. It will basically print the spaces before asterisks as required in every row.

- Again, run a loop, print the asterisk, all in one line, to complete the current row.

- Move to a new line after printing each row to maintain the right-angled triangle shape of the pattern.

```Java
class Solution {
    // Function to print pattern8
    public static void pattern8(int n) {
        
        // Outer loop which will loop for the rows.
        for (int i = 0; i < n; i++) {
            
            //This loop will print the spaces
            for(int j = 0; j < i; j++){
                System.out.print(" ");
            }
            
            // This loop will print asterisk.
            for (int j = 0; j < 2*n-(2*i+1); j++) {
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

        sol.pattern8(N);
    }
}
```