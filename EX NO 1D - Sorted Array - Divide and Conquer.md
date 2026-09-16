
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 16.09.2026
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm
1. Start and initialize two pointers p1 and p2 for the two sorted arrays.
2. Compare the elements at both pointers and select the smaller element, moving its pointer forward.
3. Continue this process until reaching the middle position of the combined arrays.
4. If the total length is odd, return the middle element; if even, take the average of the two middle elements.
5. Print the calculated median of the two sorted arrays. 

## Program:
```
/*
Program to implement Reverse a String
Developed by: RIYA P L
Register Number:  212223240141
*/
import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;

    // Get the smaller value between nums1[p1] and nums2[p2], and move the pointer forward
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; // Should not reach here if input is valid
    }

    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
       int m=nums1.length, n=nums2.length;
       int total=m+n;
       if(total%2==0){
           for(int i=0;i<total/2-1;i++) getMin(nums1,nums2);
           return (double) (getMin(nums1,nums2)+getMin(nums1,nums2))/2;
       }
       else{
           for(int i=0;i<total/2;i++) getMin(nums1,nums2);
           return getMin(nums1,nums2);
       }
    }

    // Main method with user input
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        // Input for nums2
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}

```

## Output:
<img width="982" height="312" alt="image" src="https://github.com/user-attachments/assets/1f07d9b6-72a5-41d9-9a29-3e7a0c35b744" />



## Result:
The program successfully implemented and the expected output is verified.
