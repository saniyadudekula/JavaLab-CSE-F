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
![6a output](https://github.com/user-attachments/assets/3df7c855-be86-4a96-b534-e019bf2076a9)







# EXPERIMENT 6b
## TITTLE:) Illustrating Multiple catch clauses java
# SOURCE CODE
# ArithmeticOperation
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
 // MultipleCatchDemo.java
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
![6b output](https://github.com/user-attachments/assets/784b2b3b-b7fc-4dd5-a860-58f910811eef)






# EXPERIMENT 6c
## TITTLE:)JAVA program for creation of Java Built-in Exceptions
```
// DivisionOperation.java

import java.util.Scanner;

public class DivisionOperation {

    public void divideNumber() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter an integer to divide 100: ");
        int n = sc.nextInt();

        int result = 100 / n;   // May cause ArithmeticException
        System.out.println("Result = " + result);
    }
}

// ArrayExceptionDemo.java

public class ArrayExceptionDemo {

    public void accessArray() {
        int[] arr = {10, 20, 30};

        // Intentionally accessing invalid index
        System.out.println("Accessing element: " + arr[5]);
    }
}

// NumberFormatDemo.java
import java.util.Scanner;

public class NumberFormatDemo {

    public void convertStringToInt() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number as text: ");
        String s = sc.next();

        int num = Integer.parseInt(s);  // May cause NumberFormatException
        System.out.println("Converted number = " + num);
    }
}

// BuiltInExceptionDemo.java
public class BuiltInExceptionDemo {

    public static void main(String[] args) {

        try {
            DivisionOperation d = new DivisionOperation();
            d.divideNumber();

            ArrayExceptionDemo a = new ArrayExceptionDemo();
            a.accessArray();

            NumberFormatDemo n = new NumberFormatDemo();
            n.convertStringToInt();
        }

        catch (ArithmeticException e) {
            System.out.println("ArithmeticException: division by zero.");
        }

        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("ArrayIndexOutOfBoundsException: invalid index.");
        }

        catch (NumberFormatException e) {
            System.out.println("NumberFormatException: invalid numeric format.");
        }

        catch (Exception e) {
            System.out.println("Some other exception occurred.");
        }

        System.out.println("Program continues...");
    }
}
```
# OUTPUT:
![6c output](https://github.com/user-attachments/assets/69ae7a05-62f1-4859-ab50-a0d3c82b4b4c)

