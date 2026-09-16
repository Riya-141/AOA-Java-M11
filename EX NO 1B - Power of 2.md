# EX 1B Power of 2
## DATE: 16.09.2026
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

## Algorithm
1. Get input from the user as an integer.
2. Using recursive function, call the function to perform power of two.
3. Check whether the given number is greater than or equal to 0.
4. Perform recursive call to calculate whether the given number is power of two.
5. Print true if it is a power of two, else false.

## Program:
```
/*
Program to calculate power of two.
Developed by: RIYA P L
Register Number:  212223240141
*/
import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
     if(n<=0) return false;
     return (n&(n-1))==0;
     
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}

```

## Output:
<img width="387" height="202" alt="image" src="https://github.com/user-attachments/assets/4133c303-5c49-4b37-82c4-5669de058fc9" />



## Result:
The program successfully implemented and the expected output is verified.
