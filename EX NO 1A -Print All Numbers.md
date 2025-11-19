
# EX 1A Print All Numbers 
## DATE: 06/08/2025
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1. Start the program and read the value of N from the user.
2. Check whether N is greater than 0.
3. If N ≤ 0, display an error message indicating invalid input.
4. If N > 0, initialize a loop variable i = 1.
5.Repeat printing i and increment it by 1 until i becomes greater than N.

## Program:

```

/*
 Program: Print numbers from 1 to N
 Developed by: Mohammed Muzammil A
 Register Number: 212222040103
*/



import java.util.Scanner;

public class Print {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt();
        if (N <= 0) {
            System.out.println("Invalid input. N must be greater than 0.");
        } else {
            for (int i = 1; i <= N; i++) {
                System.out.print(i + " ");
            }
        }
    }
}

```

## Output:

<img width="1331" height="233" alt="1a" src="https://github.com/user-attachments/assets/99f3de26-f3dc-4b4c-b557-293b9efd80e8" />




## Result:
The program successfully print all the numbers from 1 to N. 
