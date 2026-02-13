# EXPERIMENT5A
## TITTLE 5A)what interface can be achived
```
// Interface
interface Sortable {
    void sort(int[] arr);
}

// BubbleSort class implementing Sortable
public class BubbleSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {

                if (arr[j] > arr[j + 1]) {
                    // swap
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}

// SelectionSort class implementing Sortable
public class SelectionSort implements Sortable {

    public void sort(int[] arr) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {

            int minIndex = i;

            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[minIndex]) {
                    minIndex = j;
                }
            }

            // swap
            int temp = arr[minIndex];
            arr[minIndex] = arr[i];
            arr[i] = temp;
        }
    }
}

// Main class
public class TestSort {

    public static void main(String[] args) {

        int[] arr1 = {5, 2, 9, 1, 3};

        Sortable ref;

        ref = new BubbleSort();
        ref.sort(arr1);

        System.out.println("Array sorted using BubbleSort:");
        display(arr1);

        int[] arr2 = {8, 4, 7, 6, 2};

        ref = new SelectionSort();
        ref.sort(arr2);

        System.out.println("Array sorted using SelectionSort:");
        display(arr2);
    }
    static void display(int[] arr)
{
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }

}
```
# output
![5a output](https://github.com/user-attachments/assets/0d65fa4f-7fac-43b7-91c4-f99e3cf3477f)




# EXPERIMENT5B
## TITTLE 5B)RUNTIME POLYMORPHISM
```
// Base class
class Vehicle {

    void run() {
        System.out.println("Vehicle is running");
    }
}

// Subclass Car
class Car extends Vehicle {

    @Override
    void run() {
        System.out.println("Car is running on four wheels");
    }
}

// Subclass Bike
class Bike extends Vehicle {

    @Override
    void run() {
        System.out.println("Bike is running on two wheels");
    }
}

// Main class
public class TestVehicle {

    public static void main(String[] args) {

        Vehicle v;   // base class reference

        v = new Car();
        v.run();     // calls Car's run()

        v = new Bike();
        v.run();     // calls Bike's run()

        v = new Vehicle();
        v.run();     // calls Vehicle's run()
    }
}
```
# OUTPUT
![5B OUTPUT](https://github.com/user-attachments/assets/abdec3b3-1a0e-4097-903f-ed514ed79e01)

