# Largest Element

Given an array of integers nums, return the value of the largest element in the array

|Example 1  |Example 2  |
|---------  |---------  |
|Input: nums = [3, 3, 6, 1]  |Input: nums = [3, 3, 0, 99, -40]  |
|Output: 6  |Output: 99  |
|Explanation: The largest element in array is 6  |Explanation: The largest element in array is 99  |

- Constraints :
>1 <= nums.length <= 105
>-104 <= nums[i] <= 104
>nums may contain duplicate elements.

## Brute Approach :

- Sort the array in ascending order using in-built methods.

- Return the element at the last index of the array.

```Java
import java.util.*;

class Solution {
    public static int largestElement(int[]  nums) {
        // Sort array
        Arrays.sort(nums);

        /*Largest element will be at 
        the last index of the array.*/
        int largest = nums[nums.length - 1];

        //Return the largest element in array.
        return largest;
    }

    public static void main(String[] args) {
        int[] nums = {3,2,1,5,2};

        //Make an intance of the Solution class
        Solution sol = new Solution();

        int largest = sol.largestElement(nums);

        // Print the largest element.
        System.out.print(largest);
    }
}
```

## Complexity Analysis : 

- Time Complexity: O(N * logN)
- Space Complexity: O(log(n))

---

## Optimal Approach : 

- Create a max variable and initialize it with arr[0], as in the beginning the first element should be maximum.

- Iterate in the array and compare it with other elements to update the maximum.

- If any element is greater than the max value, update max value with the element’s value and at last return the max.

```Java
import java.util.*;

class Solution {
    public int largestElement(int[] nums) {
        // Initialize max as the first element
        int max = nums[0];

        // Traverse the entire array
        for (int i = 1; i < nums.length; i++) {

            /* If current element is greater
            than max, update max*/
            if (nums[i] > max) {
                max = nums[i];
            }

        }
        // Return the largest element found
        return max;
    }

    public static void main(String[] args) {
        int[] nums = {3,2,1,5,2};

        // Create an instance of the Solution class
        Solution sol = new Solution();

        // Find and print the largest element in the array
        System.out.println("The largest element in the array is: " + sol.largestElement(nums));
    }
}
```

## Complexity Analysis : 

- Time Complexity: O(N)
- Space Complexity: O(1)