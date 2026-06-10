# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1.Start   

2.Read the number of elements (e.g., number of heartbeat readings).

3.Store all readings in an array.

4.Call a recursive function findMin(arr, index)
If index == arr.length - 1, return arr[index]
Else return min(arr[index], findMin(arr, index + 1))

5.Print the minimum value returned by the recursive function.

6.End

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

*/

import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) {
        if (i == n - 1) {
            return arr[i];
        }

    
        int minRest = getMin(arr, i + 1, n);
       
        return Math.min(arr[i], minRest);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}

```

## Output:

<img width="649" height="254" alt="image" src="https://github.com/user-attachments/assets/1da02a5e-689f-48d2-a043-351435e32ef6" />


## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully


# Ex2 Count how many times a number appears in an array recursively.
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1.Start

2.Read the size of the array and input all elements into the array.

3.Read the target number whose frequency you want to count.

4.Call the recursive function countOccurrences(arr, index, target) If index == arr.length, return 0 If arr[index] == target, return 1 + countOccurrences(arr, index + 1, target) Else return countOccurrences(arr, index + 1, target)

5.Display the returned count as the total number of occurrences.

## Program:
```
/*
Program Count how many times a number appears in an array recursively.

*/

import java.util.Scanner;

public class CountOccurrences {

    // Recursive function to count occurrences of a target number
    public static int countOccurrences(int[] arr, int n, int target) {
        //write your code here
        if (n == 0) {
            return 0;
        }

        // Check the last element and add 1 if it matches the target
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input: Size of array
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }

        // Input: Array elements
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        // Input: Target number to count
        int target = scanner.nextInt();

        // Compute and display result
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}

```

## Output:

<img width="1027" height="611" alt="image" src="https://github.com/user-attachments/assets/4003ed2c-aaa4-436e-a344-6ba6de2fc178" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.


# EX3 Write a program to count the number of digits in an integer.
## AIM:
To write a java program to implement Tower of Hanoi

## Algorithm
1. Start the program.
2. Read an integer from the user.
3. Define a recursive function countDigits() that counts digits by dividing the number by 10 each time.
4. Base condition: if the number is 0, return 0.
5. Recursive step: return 1 + countDigits(number / 10).
6. Display the total count of digits.
7. Stop the program

## Program:
```
/*
Program to to count the number of digits in an integer

*/
import java.util.Scanner;

public class RotatedArraySearch {

    public static int search(int[] arr, int left, int right, int target) {
        if (left > right) return -1;

        int mid = (left + right) / 2;

        if (arr[mid] == target) return mid;

        
        if (arr[left] <= arr[mid]) {
            if (target >= arr[left] && target < arr[mid]) {
                return search(arr, left, mid - 1, target);
            } else {
                return search(arr, mid + 1, right, target);
            }
        }
        
        else {
            if (target > arr[mid] && target <= arr[right]) {
                return search(arr, mid + 1, right, target);
            } else {
                return search(arr, left, mid - 1, target);
            }
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int size = scanner.nextInt();
        if (size <= 0) return;

        int[] arr = new int[size];

        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        int target = scanner.nextInt();

        int index = search(arr, 0, size - 1, target);

        if (index != -1) {
            System.out.println("Element " + target + " found at index: " + index);
        } else {
            System.out.println("Element " + target + " not found in the array.");
        }

        scanner.close();
    }
}
```

## Output:


<img width="1283" height="751" alt="image" src="https://github.com/user-attachments/assets/eb600e14-3a99-4e0a-9a38-620fc6cb34d4" />




## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.


# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start the program.
2. Read the dimensions of both matrices (rows and columns).
3. Check whether Matrix A and Matrix B have the same dimensions.
4. If not, display “Matrices are not of same dimension” and stop.
5. Read Matrix A and check each element:
6. If every element is odd, continue.
7. If any element is even, mark A as invalid and stop further checking.
8. If both matrices are valid, compute the resultant matrix (e.g., A + B or any operation specified).
9. Determine the nature of the resultant matrix:
10. If all elements are odd, print “Resultant matrix is an Odd Matrix”.
11. If all elements are even, print “Resultant matrix is an Even Matrix”.
12. Display the Resultant Matrix.
13. Stop the program.

## Program:
```
Program to ind the nature of resultant matrrix.

*/
import java.util.Scanner;

public class MatrixAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int rows = sc.nextInt();
        int cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] result = new int[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result[i][j] = A[i][j] + B[i][j];
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }

       
    }
}
```

## Output:

<img width="422" height="624" alt="image" src="https://github.com/user-attachments/assets/389dd1b1-f2ce-4a47-8eec-13d0ebbb8316" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.


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
