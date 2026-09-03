# Pattern 15 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-15](https://static.takeuforward.org/content/ProblemSetter-8ZjzMsZW)

- Constraints

    1 <= n <= 100

## Approach : 

- Use a for loop to iterate from 0 to N-1, where N is the number of rows. This loop will ensure to print each row of the pattern.

- The inner loop will run for i times and print alphabets from 'A' to 'A' + (N-row number-1).

- After completing a row give a line break, to make sure next row gets printed as well.

```Java
class Solution {
    // Function to print pattern15
    void pattern15(int n) {
        // Outer loop for the number of rows.
        for (int i = 0; i < n; i++) {
            
            /* Inner loop runs (n - i) times and
            prints (n - i) alphabets starting from 'A'.*/
            for (char ch = 'A'; ch<='A'+(n-i-1);ch++) {
                System.out.print(ch);
            }
            
            /*As soon as the letters for each iteration
            are printed, we move to the next row and give
            a line break otherwise all letters would get
            printed in 1 line.*/
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 5;

        // Create an instance of Solution class
        Solution sol = new Solution();

        sol.pattern15(N);
    }
}
```