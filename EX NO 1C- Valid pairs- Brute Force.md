
# EX 1C Valid Pairs using Brute Force Approach
## DATE: 16.09.2026
## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

## Algorithm
1. Start and initialize count = 0.
2. Use two loops to select every pair of elements (i, j) where i < j.
3. Calculate the absolute difference |nums[i] - nums[j]|.
4. If the difference equals k, increment count.
5. Return/print count as the number of valid pairs.

## Program:
```
/*
Program to implement Reverse a String
Developed by: RIYA P L
Register Number:  212223240141
*/
import java.util.*;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        int count=0;
      for(int i=0;i<nums.length;i++){
      for(int j=i+1;j<nums.length;j++){
      if(Math.abs(nums[i]-nums[j])==k) count++;
      }
      
      }
    return count;

    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}

```

## Output:
<img width="392" height="272" alt="image" src="https://github.com/user-attachments/assets/9d0bb444-bf0e-4da8-bf62-bf9d53081247" />



## Result:
The program successfully implemented and the expected output is verified.
