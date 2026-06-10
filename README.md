# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Read the number of elements n and input all n integers into an array arr.
2. Start the recursive function getMin(arr, 0, n) to find the minimum element.
3. Inside the recursive function, check if the current index i is the last index (i      == n−1).If yes, return arr[i] as the minimum.
4. Otherwise, recursively call getMin(arr, i+1, n) to find the minimum of the remaining elements.
5. Compare the current element arr[i] with the minimum of the rest and return the smaller value.   

## Program:


```
import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) 
    {
        
        if (i == n - 1)
            return arr[i];
        
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```

## Output:

<img width="576" height="303" alt="image" src="https://github.com/user-attachments/assets/3f8f606d-2c09-4be2-bb25-3137c564b823" />

## Result:
Thus the JAVA program ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully


# Ex2 Count how many times a number appears in an array recursively.

## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Read the value of n, input n elements into array arr, and read the number key whose occurrences must be counted.
2. Call the recursive function countOccurrences(arr, n, 0, key) starting from index 0.
3. Inside the recursive function, check if the current index equals n;if yes, return 0 because the entire array has been checked.
4. If arr[index] equals key, return 1 + countOccurrences(arr, n, index + 1, key);otherwise return countOccurrences(arr, n, index + 1, key).
5. Return the final count to the main program and print how many times key appears in the array.   

## Program:


```
import java.util.Scanner;

public class CountOccurrencesRecursive {
    
    public static int countOccurrences(int[] arr, int n, int index, int key) {
        if (index == n) {
            return 0; 
        }
        if (arr[index] == key) {
            return 1 + countOccurrences(arr, n, index + 1, key);
        } else {
            return countOccurrences(arr, n, index + 1, key);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

    
        int n = sc.nextInt();

        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int key = sc.nextInt();

        int count = countOccurrences(arr, n, 0, key);

        System.out.println("The number " + key + " appears " + count + " time(s) in the array.");
    }
}

```

## Output:

<img width="679" height="380" alt="image" src="https://github.com/user-attachments/assets/f8c606ed-86b7-4c72-9b48-ae94ce15babb" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.

# EX3 Write a program to count the number of digits in an integer.

## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm

1. Read the input number Take an integer num from the user.
2. Convert the number to a non-negative value Use Math.abs(num) and store it in n to handle negative numbers.
3. Check if the number is zero If n == 0, set digit count to 1 (since zero has one digit).
4. Count digits for non-zero numbers Repeatedly divide n by 10 and increment the counter until n becomes 0.
5. Display the digit count Output the total number of digits.
    
## Program:


```

import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        int count = 0;
        int n = Math.abs(num); 

        if (n == 0) {
            count = 1; 
        } else {
            while (n > 0) {
                n /= 10; 
                count++;
            }
        }

        System.out.println("Number of digits: " + count);
    }
}
```

## Output:
<img width="733" height="328" alt="01" src="https://github.com/user-attachments/assets/912ff986-b3d6-4ddf-ad81-ae28ea3a19f5" />

## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.

# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?

## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Read matrix dimensions Input the number of rows r and columns c.
2. Read elements of Matrix A Fill the 2D array A[r][c] by reading integers row-wise.
3. Read elements of Matrix B Fill the 2D array B[r][c] similarly by reading integers row-wise.
4. Add corresponding elements of both matrices For each position (i, j), compute A[i][j] + B[i][j].
5. Print the resulting matrix Output each sum in matrix form, one row per line. 

## Program:


```
import java.util.*;

public class MatrixAddShort {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int r = sc.nextInt(), c = sc.nextInt();
        int[][] A = new int[r][c], B = new int[r][c];

        for (int i = 0; i < r; i++)  
            for (int j = 0; j < c; j++)
                A[i][j] = sc.nextInt();

        for (int i = 0; i < r; i++)  
            for (int j = 0; j < c; j++)
                B[i][j] = sc.nextInt();

       
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++)
                System.out.print((A[i][j] + B[i][j]) + " ");
            System.out.println();
        }
    }
}

```

## Output:
<img width="451" height="704" alt="image" src="https://github.com/user-attachments/assets/ea8c25ed-d97b-4b5b-a2e2-5275de76a9a6" />

## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.

# Ex5 Count Inversions in an Array

## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Read n and the array elements.
2. Use merge sort to split the array into halves.
3. Count inversions in the left half and right half.
4. Merge the halves and count cross-inversions when right element < left element.
5. Add all inversion counts and print the result.   

## Program:

```
import java.util.Scanner;

public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        for (int i = 0; i < leftArr.length; i++) leftArr[i] = arr[left + i];
        for (int i = 0; i < rightArr.length; i++) rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left, swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (leftArr.length - i); // Count inversions
                
            }
       
        }

        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return swaps;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}

```

## Output:

<img width="466" height="401" alt="image" src="https://github.com/user-attachments/assets/b2686bb6-2298-4e84-bfaf-02f66055ae6c" />


## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.

