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
