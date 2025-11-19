
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 20/08/2025
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm
1. Read the sizes of the two arrays and input all elements into nums1 and nums2.
2. Calculate the total length and determine the middle positions (mid1 and mid2) needed for finding the median.
3. Merge the two sorted arrays conceptually by repeatedly choosing the smaller current element using pointers p1 and p2.
4. Keep track of the current and previous values while merging until reaching the middle position.
5. If the total length is even, return the average of the two middle values; otherwise return the current middle value.


## Program:
```
/*
Program to return median of two sorted arrays
Developed by: Mohammed Muzammil A
Register Number:  212222040103
*/


import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; 
    }

    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int total = nums1.length + nums2.length;
        int mid1 = (total - 1) / 2;
        int mid2 = total / 2;
        int count = 0;
        int curr = 0, prev = 0;

        while (count <= mid2) {
            prev = curr;
            curr = getMin(nums1, nums2);
            count++;
        }

        if (total % 2 == 0)
            return (prev + curr) / 2.0;
        else
            return curr;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        int m = sc.nextInt();
        int[] nums1 = new int[m];
        
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);

        sc.close();
    }
}

```

## Output:
<img width="948" height="288" alt="1d" src="https://github.com/user-attachments/assets/a6340f9b-8b10-4823-9bd5-8d75c3f95bb1" />




## Result:
The program successfully implemented and the expected output is verified.
