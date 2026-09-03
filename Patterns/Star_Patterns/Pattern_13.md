# Pattern 13 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-13](https://static.takeuforward.org/content/ProblemSetter-DK55vapT)

- Constraints

    1 <= n <= 100

## Approach : 

- Iterate from 1 to N, where N is the number of rows.

- Inside this loop, take another loop to define the number of columns needed in each row. Now print the numbers strating from 1 and a space. Then increment the number by 1 every time.

- After completion of a row, make sure to give a line break to print the next rows as well.

```Java
class Solution {
    // Function to print pattern13
    void pattern13(int n) {
        // starting the number
        int num = 1;

        // Outer loop for the number of rows.
        for (int i = 1; i <= n; i++) {
            
            /*Inner loop will loop for i times and
            print numbers increasing by 1 each time*/
            for (int j = 1; j <= i; j++) {
                System.out.print(num + " ");
                num = num + 1;
            }
            /* As soon as the numbers for each iteration
            are printed, we move to the next row and give
            a line break otherwise all numbers would get
            printed in 1 line*/
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int N = 5;

        // Create an instance of Solution class
        Solution sol = new Solution();

        sol.pattern13(N);
    }
}
```