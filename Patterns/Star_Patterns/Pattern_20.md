# Pattern 20 :

Given an integer n. You need to recreate the pattern given below for any value of N. Let's say for N = 5, the pattern should look like as below:

![Pattern-20](https://static.takeuforward.org/content/ProblemSetter-PowWIHqE)

- Constraints

    1 <= n <= 100

## Approach : 

- Start by initializing spaces to 2*N - 2. This variable tracks the number of spaces between the two sets of stars in each row, where N is the number of rows.

- Use an outer loop (for loop) to iterate from 1 to 2*N- 1. This loop controls the number of rows printed for both the upper and lower halves of the pattern.

- Inside the loop, calculate stars: For the first half (when row number <= N), stars starts from 1 and increments with each row. For the second half (when row > N), stars decreases with each row.

- Use nested loops to print stars, spaces, the second set of stars, mirroring the first set. After printing stars and spaces for each row, adjust spaces.

- If row < N, decrease spaces by 2 to gradually reduce the space between stars as rows progress towards the middle, else, increase spaces by 2 to gradually increase the space as rows move away from the middle.

- After completing a row give a line break, to make sure next row gets printed as well.

```Java
import java.util.*;
class Solution {
    // Function to print pattern20
    public void pattern20(int n) {
        // Initialising the spaces.
        int spaces = 2*n-2;
        
        // Outer loop to print the row.
        for(int i = 1; i <= 2*n-1; i++){
            // Stars for first half
            int stars = i;
            
            // Stars for the second half.
            if(i > n) stars = 2*n - i;
            
            // For printing the stars
            for(int j = 1; j <= stars; j++){
                System.out.print("*");
            }
            
            // For printing the spaces
            for(int j = 1; j <= spaces; j++){
                System.out.print(" ");
            }
            
            // For printing the stars
            for(int j = 1; j <= stars; j++){
                System.out.print("*");
            }
            
            // Give a line break for new row.
            System.out.println();
            
            if(i < n) spaces -= 2;
            else spaces += 2;
        }
    }

    public static void main(String[] args) {
        int N = 5;
        
        // Create an instance of Solution class
        Solution sol = new Solution();
        
        sol.pattern20(N);
    }
}
```