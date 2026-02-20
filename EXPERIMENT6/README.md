# EXPERIMENT6a
## TITTLE:) exception handling mechanism in java
```
// ArrayInput.java
import java.util.Scanner;

public class ArrayInput {

    public int[] readArray() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the size of the array: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        return arr;
    }
}
```
```JAVA
// ArrayAccess.java
import java.util.Scanner;

public class ArrayAccess {

    public void accessElement(int[] arr) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the index to access: ");
        int index = sc.nextInt();

        try {
            System.out.println("Element at index " + index + " is: " + arr[index]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println(
                "Invalid index! Please enter an index between 0 and " + (arr.length - 1)
            );
        }
    }
}
```
```JAVA
// ExceptionHandlingDemo.java

public class ExceptionHandlingDemo {

    public static void main(String[] args) {

        ArrayInput input = new ArrayInput();
        int[] array = input.readArray();

        ArrayAccess access = new ArrayAccess();
        access.accessElement(array);
    }
}
```
# OUTPUT:






# EXPERIMENT 6b
## TITTLE:) Illustrating Multiple catch clauses java
```
// ArithmeticOperation.java
import java.util.Scanner;

public class ArithmeticOperation {

    public int divide() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        int result = a / b;   // May throw ArithmeticException
        System.out.println("Division Result = " + result);

        return result;
    }
}
```
```JAVA
// ArrayOperation.java

import java.util.Scanner;

public class ArrayOperation {

    public void accessArray() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter size of array: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter " + n + " array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.print("Enter index to access array element: ");
        int index = sc.nextInt();

        System.out.println("Element at index " + index + " = " + arr[index]);
    }
}
```
```JAVA
# // MultipleCatchDemo.java
import java.util.InputMismatchException;

public class MultipleCatchDemo {

    public static void main(String[] args) {

        try {
            ArithmeticOperation ao = new ArithmeticOperation();
            ao.divide();

            ArrayOperation ar = new ArrayOperation();
            ar.accessArray();
        }

        catch (ArithmeticException e) {
            System.out.println("Error: Division by zero is not allowed.");
        }

        catch (InputMismatchException e) {
            System.out.println("Error: Please enter numeric values only.");
        }

        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Invalid array index.");
        }

        catch (Exception e) {
            System.out.println("Some other error occurred.");
        }

        System.out.println("Program continues...");
    }
}
```
# OUTPUT:

