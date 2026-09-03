# Pattern 9 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-9](https://static.takeuforward.org/content/ProblemSetter-lFiwQ3fG)

- Constraints

    1 <= n <= 100

## Approach : 

- This pattern is a combination of the pyramid and an inverted pyramid. First, print the pyramid and then the inverted one.

- Use nested for loops to print the pyramid. First, print the spaces using a for loop, and then the required asterisks using a second for loop.

- After this, give a line break to print the next row. Follow the same process to print the inverted pyramid.

```Java
class Solution {
    // Function to print pattern9
    public static void pattern9(int n) {
        erectPyramid(n);
        invertedPyramid(n);
    }

    private static void erectPyramid(int n) {
        // Outer loop which will loop for the rows.
        for (int i = 0; i < n; i++) {
            // For printing the spaces before stars in each row
            for (int j = 0; j < n - i - 1; j++) {
                System.out.print(" ");
            }

            // For printing the stars in each row
            for (int j = 0; j < 2 * i + 1; j++) {
                System.out.print("*");
            }

            /* As soon as the stars for each iteration are printed,
            we move to the next row and give a line break */
            System.out.println();
        }
    }

    private static void invertedPyramid(int n) {
        // Outer loop which will loop for the rows.
        for (int i = 0; i < n; i++) {
            // For printing the spaces before stars in each row
            for (int j = 0; j < i; j++) {
                System.out.print(" ");
            }

            // For printing the stars in each row
            for (int j = 0; j < 2 * n - (2 * i + 1); j++) {
                System.out.print("*");
            }

            /* As soon as the stars for each iteration are printed,
            we move to the next row and give a line break */
            System.out.println();
        }
    }
}

class Main {
    public static void main(String[] args) {
        int N = 5;

        // Create an instance of Solution class
        Solution sol = new Solution();

        sol.pattern9(N);
    }
}
```