# Ex5 Count Inversions in an Array
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start the program.
2. Declare an integer array arr of size n.
3. Read the value of n (number of elements).
4. Read n elements and store them in the array arr.
5. Initialize a variable count to 0 to store the number of inversions.
6. Use two nested loops:
7. Outer loop variable i from 0 to n - 1
8. Inner loop variable j from i + 1 to n - 1
9. For each pair (i, j), if arr[i] > arr[j] and i < j, increment count by 1.
10. After all comparisons, print the value of count as the total number of inversions in the array.
11. Stop the program.  

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: T MOUNISH
RegisterNumber:  212223240098
*/
import java.util.Scanner;

public class FibonacciSeries {

    static int fibonacciRecursive(int n) {
        if (n == 0) return 0;
        if (n == 1) return 1;
        return fibonacciRecursive(n - 1) + fibonacciRecursive(n - 2);
    }

    static void fibonacciIterative(int n) {
        int first = 0, second = 1;
        System.out.print(first + " " + second + " ");
        for (int i = 2; i < n; i++) {
            int next = first + second;
            System.out.print(next + " ");
            first = second;
            second = next;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        System.out.println("Fibonacci Series using Recursion:");
        for (int i = 0; i < n; i++) {
            System.out.print(fibonacciRecursive(i) + " ");
        }

        System.out.println("\n");

        System.out.println("Fibonacci Series using Iteration:");
        if (n == 1) {
            System.out.println("0");
        } else if (n >= 2) {
            fibonacciIterative(n);
        }

        sc.close();
    }
}

```

## Output:


<img width="965" height="603" alt="image" src="https://github.com/user-attachments/assets/751f5842-ec80-4a0f-bb81-67b7088a5df5" />

## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
