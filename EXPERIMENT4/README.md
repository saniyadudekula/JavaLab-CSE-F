# EXPERIMENT4A
## TITTLE 4a) A JAVA PROGRAM TO IMPLEMENT SINGLE INHERITANCE
```
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String insuranceNumber;

    Employee(String name, int age, double annualSalary, int yearOfJoining, String insuranceNumber) {
        super(name, age);
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.insuranceNumber = insuranceNumber;
    }

    void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("Insurance Number: " + insuranceNumber);
    }
}

public class TestEmployee {
    public static void main(String[] args) {
        Employee emp = new Employee("Saniya", 20, 450000, 2024, "INS12345");
        emp.displayEmployeeDetails();
    }
}
```
# OUTPUT
![4A OUTPUT](https://github.com/user-attachments/assets/6d6fd9f0-9019-4e2a-b0d8-890d6d2906c0)




# EXPRIMENT4B
## TITTLE 4B)A JAVA PROGRAM TO IMPLEMENT MULTI-LEVEL INHERITANCE
```
class Bicycle {
    String pedalType;

    Bicycle(String pedalType) {
        this.pedalType = pedalType;
    }

    void displayBicycle() {
        System.out.println("Pedal Type: " + pedalType);
    }
}

class MotorBike extends Bicycle {
    String engineType;

    MotorBike(String pedalType, String engineType) {
        super(pedalType);
        this.engineType = engineType;
    }

    void displayMotorBike() {
        displayBicycle();
        System.out.println("Engine Type: " + engineType);
    }
}

class ElectricBike extends MotorBike {
    String motorType;
    int batteryCapacity;

    ElectricBike(String pedalType, String engineType, String motorType, int batteryCapacity) {
        super(pedalType, engineType);
        this.motorType = motorType;
        this.batteryCapacity = batteryCapacity;
    }

    void displayElectricBike() {
        displayMotorBike();
        System.out.println("Motor Type: " + motorType);
        System.out.println("Battery Capacity: " + batteryCapacity + " Wh");
    }
}

public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eb = new ElectricBike(
                "Standard Pedals",
                "Petrol Engine",
                "Electric Motor",
                500
        );

        eb.displayElectricBike();
    }
}
```
# OUTPUT
![4B OUTPUT](https://github.com/user-attachments/assets/8836710d-a306-416e-b845-7b5ad6911a02)





# EXPERIMENT4C
## TITTLE 4C)ABSTRACT CLASS TO FIND AREA OF DIFFERENT SHAPES
```
abstract class Figure {
    double dim1;
    double dim2;

    Figure(double dim1, double dim2) {
        this.dim1 = dim1;
        this.dim2 = dim2;
    }

    abstract double area();
}

// Rectangle class
class Rectangle extends Figure {

    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    // Override area method
    double area() {
        return dim1 * dim2;
    }
}

// Triangle class
class Triangle extends Figure {

    Triangle(double base, double height) {
        super(base, height);
    }

    // Override area method
    double area() {
        return 0.5 * dim1 * dim2;
    }
}

// Main class
public class TestFigure {
    public static void main(String[] args) {

        Figure rect = new Rectangle(10, 5);
        Figure tri = new Triangle(8, 6);

        System.out.println("Area of Rectangle: " + rect.area());
        System.out.println("Area of Triangle: " + tri.area());
    }
}
```
# OUTPUT
![4C OUTPUT](https://github.com/user-attachments/assets/3fbc2bd5-27f0-4287-9004-ec1629398541)
