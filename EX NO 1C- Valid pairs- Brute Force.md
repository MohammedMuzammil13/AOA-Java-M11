
# EX 1C Valid Pairs using Brute Force Approach
## DATE: 21/08/2025
## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

## Algorithm
1. Read the value of n and then read n integers into the array nums.
2. Read the value of k.
3. Initialize a counter variable count to 0.
4. Use two nested loops to compare every pair of elements; if the absolute difference between nums[i] and nums[j] is equal to k, increment count.
5. Print the value of count as the total number of valid pairs.
  

## Program:
```
/*
Program to count pairs with K difference
Developed by: Mohammed Muzammil A
Register Number:  212222040103
*/


import java.util.Scanner;

public class CountPairsWithDifference {

    public static int countKDifference(int[] nums, int k) {
        int count = 0;
        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (Math.abs(nums[i] - nums[j]) == k) {
                    count++;
                }
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
<img width="663" height="251" alt="1c" src="https://github.com/user-attachments/assets/6e4b56a8-1e19-417c-8517-a7a5462dd27b" />




## Result:
The program successfully implemented and the expected output is verified.
