
# EX 1B Power of 2
## DATE: 08/08/2025
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm
1. Start the program and read the integer n from the user.
2. Check if n is greater than 0.
3. Compute the expression (n & (n - 1)).
4. If n > 0 and (n & (n - 1)) == 0, then n is a power of two; otherwise it is not.
5. Print the result and end the program.


## Program:
```
/*
Program to check if n is power of two.
Developed by: Mohammed Muzammil A
Register Number:  212222040103
*/


import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
    return n > 0 && (n & (n - 1)) == 0;

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

<img width="670" height="177" alt="1b" src="https://github.com/user-attachments/assets/1dbf69e2-a5a2-478e-861b-b015bd79f9e3" />


## Result:
The program successfully implemented and the expected output is verified.
