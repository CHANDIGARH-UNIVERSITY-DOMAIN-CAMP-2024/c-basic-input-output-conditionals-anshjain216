# 1. Sum of Natural Numbers up to N
This program calculates the sum of all natural numbers from 1 to `n`, where `n` is a positive integer. The calculation is performed using the formula:

```java
import java.util.Scanner;

public class NaturalNumberSum {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a positive integer n: ");
        int n = scanner.nextInt();
        
        if (n < 1 || n > 10000) {
            System.out.println("Please enter a number between 1 and 10000.");
        } else {
            long sum = (long) n * (n + 1) / 2;
            System.out.println("Sum of natural numbers from 1 to " + n + " is: " + sum);
        }
        
        scanner.close();
    }
}
```


# 2. Check if a Number is Prime
This program checks whether a given number `n` is a prime number. A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself. 
To determine if a number is prime, the program iterates from 2 to √n and checks if `n` is divisible by any number in this range. If it is divisible, the number is not prime; otherwise, it is prime.


```java
import java.util.Scanner;

public class PrimeCheck {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number to check if it's prime: ");
        int n = scanner.nextInt();

        if (n < 2 || n > 100000) {
            System.out.println("Please enter a number between 2 and 100000.");
        } else {
            boolean isPrime = true;

            for (int i = 2; i * i <= n; i++) {
                if (n % i == 0) {
                    isPrime = false;
                    break;
                }
            }

            if (isPrime) {
                System.out.println("Prime");
            } else {
                System.out.println("Not Prime");
            }
        }

        scanner.close();
    }
}
```


# 3. Print Odd Numbers up to N
This program prints all odd numbers between 1 and `n`, inclusive. Odd numbers are integers that are not divisible by 2. These numbers are printed in ascending order, separated by spaces.
The program uses a loop to iterate over the numbers and checks if they are odd using the condition `i % 2 != 0`.

```java
import java.util.Scanner;

public class OddNumberPrinter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number to print odd numbers up to: ");
        int n = scanner.nextInt();

        if (n < 1 || n > 10000) {
            System.out.println("Please enter a number between 1 and 10000.");
        } else {
            for (int i = 1; i <= n; i++) {
                if (i % 2 != 0) {
                    System.out.print(i + " ");
                }
            }
        }
        
        scanner.close();
    }
}
```


# 4. Sum of Odd Numbers up to N
This program calculates the sum of all odd numbers from 1 to `n`. An odd number is an integer that is not divisible by 2. The program iterates through all numbers from 1 to `n`, checks if each number is odd, and accumulates the sum of odd numbers.

```java
import java.util.Scanner;

public class SumOfOddNumbers {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number to calculate the sum of odd numbers up to: ");
        int n = scanner.nextInt();

        if (n < 1 || n > 10000) {
            System.out.println("Please enter a number between 1 and 10000.");
        } else {
            int sum = 0;
            for (int i = 1; i <= n; i++) {
                if (i % 2 != 0) {
                    sum += i;
                }
            }
            System.out.println("Sum of odd numbers from 1 to " + n + " is: " + sum);
        }
        
        scanner.close();
    }
}
```


# 5. Print Multiplication Table of a Number
This program prints the multiplication table of a given number `n`. A multiplication table for a number `n` consists of products of `n` with integers from 1 to 10. For example, the multiplication table for 3 is:

```java
import java.util.Scanner;

public class MultiplicationTable {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number to print the multiplication table: ");
        int n = scanner.nextInt();

        if (n < 1 || n > 100) {
            System.out.println("Please enter a number between 1 and 100.");
        } else {
            for (int i = 1; i <= 10; i++) {
                System.out.println(n + " × " + i + " = " + (n * i));
            }
        }

        scanner.close();
    }
}
```


# 6. Count digits in a number

```java
import java.util.Scanner;

public class CountDigits {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();

        int count = 0;
        while (n != 0) {
            n /= 10;
            count++;
        }

        System.out.println("Number of digits: " + count);

        scanner.close();
    }
}
```

# 7. Reverse a number

```java
import java.util.Scanner;

public class ReverseNumber {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();

        int reversed = 0;
        while (n != 0) {
            int digit = n % 10;
            reversed = reversed * 10 + digit;
            n /= 10;
        }

        System.out.println("Reversed number: " + reversed);

        scanner.close();
    }
}
```

# 8. Find the Largest Digit in a Number

```java
import java.util.Scanner;

public class LargestDigit {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();

        int largestDigit = -1;

        while (n > 0) {
            int digit = n % 10;
            if (digit > largestDigit) {
                largestDigit = digit;
            }
            n /= 10;
        }

        System.out.println("Largest digit: " + largestDigit);

        scanner.close();
    }
}
```

# 9. Check if number is palindrome or not 

```java
import java.util.Scanner;

public class PalindromeNumber {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();

        int originalNumber = n;
        int reversed = 0;

        while (n != 0) {
            int digit = n % 10;
            reversed = reversed * 10 + digit;
            n /= 10;
        }

        if (originalNumber == reversed) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not Palindrome");
        }

        scanner.close();
    }
}
```


# 10. Find the Sum of Digits of a Number

```java
import java.util.Scanner;

public class SumOfDigits {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();

        int sum = 0;
        while (n > 0) {
            sum += n % 10;
            n /= 10;
        }

        System.out.println("Sum of digits: " + sum);

        scanner.close();
    }
}
```

# 11. Function overloading in calculating area

```java
import java.util.Scanner;

public class AreaCalculator {

    // Method to calculate area of a circle
    public double calculateArea(double radius) {
        return Math.PI * radius * radius;
    }

    // Method to calculate area of a rectangle
    public double calculateArea(double length, double width) {
        return length * width;
    }

    // Method to calculate area of a triangle
    public double calculateArea(double base, double height) {
        return 0.5 * base * height;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        AreaCalculator calculator = new AreaCalculator();

        System.out.println("Choose the shape (1: Circle, 2: Rectangle, 3: Triangle): ");
        int choice = scanner.nextInt();

        switch (choice) {
            case 1: // Circle
                System.out.print("Enter the radius of the circle: ");
                double radius = scanner.nextDouble();
                System.out.println("Area of Circle: " + calculator.calculateArea(radius));
                break;

            case 2: // Rectangle
                System.out.print("Enter the length of the rectangle: ");
                double length = scanner.nextDouble();
                System.out.print("Enter the width of the rectangle: ");
                double width = scanner.nextDouble();
                System.out.println("Area of Rectangle: " + calculator.calculateArea(length, width));
                break;

            case 3: // Triangle
                System.out.print("Enter the base of the triangle: ");
                double base = scanner.nextDouble();
                System.out.print("Enter the height of the triangle: ");
                double height = scanner.nextDouble();
                System.out.println("Area of Triangle: " + calculator.calculateArea(base, height));
                break;

            default:
                System.out.println("Invalid choice.");
        }

        scanner.close();
    }
}
```

# 12. Function Overloading with Hierarchical Structure

```java
import java.util.Scanner;

public class SalaryCalculator {

    // Method to calculate salary of an Intern
    public double calculateSalary(double stipend) {
        return stipend;
    }

    // Method to calculate salary of a Regular Employee
    public double calculateSalary(double baseSalary, double bonuses) {
        return baseSalary + bonuses;
    }

    // Method to calculate salary of a Manager
    public double calculateSalary(double baseSalary, double bonuses, double incentives) {
        return baseSalary + bonuses + incentives;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        SalaryCalculator calculator = new SalaryCalculator();

        System.out.println("Enter details for Intern:");
        System.out.print("Stipend: ");
        double stipend = scanner.nextDouble();
        System.out.println("Intern Salary: " + calculator.calculateSalary(stipend));

        System.out.println("Enter details for Regular Employee:");
        System.out.print("Base Salary: ");
        double baseSalary = scanner.nextDouble();
        System.out.print("Bonuses: ");
        double bonuses = scanner.nextDouble();
        System.out.println("Regular Employee Salary: " + calculator.calculateSalary(baseSalary, bonuses));

        System.out.println("Enter details for Manager:");
        System.out.print("Base Salary: ");
        double managerBaseSalary = scanner.nextDouble();
        System.out.print("Bonuses: ");
        double managerBonuses = scanner.nextDouble();
        System.out.print("Performance Incentives: ");
        double incentives = scanner.nextDouble();
        System.out.println("Manager Salary: " + calculator.calculateSalary(managerBaseSalary, managerBonuses, incentives));

        scanner.close();
    }
}
```

# 13. Encapsulation with Employee Details

```java
import java.util.Scanner;

class Employee {
    // Private attributes
    private int employeeId;
    private String employeeName;
    private double employeeSalary;

    // Public setter for employeeId
    public void setEmployeeId(int employeeId) {
        this.employeeId = employeeId;
    }

    // Public getter for employeeId
    public int getEmployeeId() {
        return employeeId;
    }

    // Public setter for employeeName
    public void setEmployeeName(String employeeName) {
        this.employeeName = employeeName;
    }

    // Public getter for employeeName
    public String getEmployeeName() {
        return employeeName;
    }

    // Public setter for employeeSalary
    public void setEmployeeSalary(double employeeSalary) {
        this.employeeSalary = employeeSalary;
    }

    // Public getter for employeeSalary
    public double getEmployeeSalary() {
        return employeeSalary;
    }

    // Method to display employee details
    public void displayDetails() {
        System.out.println("Employee ID: " + getEmployeeId());
        System.out.println("Employee Name: " + getEmployeeName());
        System.out.println("Employee Salary: " + getEmployeeSalary());
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Creating an Employee object
        Employee employee = new Employee();

        // Accepting input for employee details
        System.out.print("Enter Employee ID: ");
        employee.setEmployeeId(scanner.nextInt());

        scanner.nextLine(); // Consume newline

        System.out.print("Enter Employee Name: ");
        employee.setEmployeeName(scanner.nextLine());

        System.out.print("Enter Employee Salary: ");
        employee.setEmployeeSalary(scanner.nextDouble());

        // Displaying employee details
        employee.displayDetails();

        scanner.close();
    }
}
```

# 14. Inheritance with Student and Result Classes.

```java
import java.util.Scanner;

// Base class: Student
class Student {
    private int rollNumber;
    private String name;

    public void setRollNumber(int rollNumber) {
        this.rollNumber = rollNumber;
    }

    public int getRollNumber() {
        return rollNumber;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

// Derived class: Result
class Result extends Student {
    private int subject1, subject2, subject3;
    private int total;
    private double percentage;

    public void setMarks(int subject1, int subject2, int subject3) {
        this.subject1 = subject1;
        this.subject2 = subject2;
        this.subject3 = subject3;
        calculateTotalAndPercentage();
    }

    private void calculateTotalAndPercentage() {
        total = subject1 + subject2 + subject3;
        percentage = (total / 3.0);
    }

    public void displayResult() {
        System.out.println("Roll Number: " + getRollNumber());
        System.out.println("Name: " + getName());
        System.out.println("Marks in Subject 1: " + subject1);
        System.out.println("Marks in Subject 2: " + subject2);
        System.out.println("Marks in Subject 3: " + subject3);
        System.out.println("Total Marks: " + total);
        System.out.println("Percentage: " + percentage + "%");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Creating an object of Result (derived class)
        Result result = new Result();

        // Accepting student details
        System.out.print("Enter Roll Number: ");
        result.setRollNumber(scanner.nextInt());

        scanner.nextLine(); // Consume newline character

        System.out.print("Enter Name: ");
        result.setName(scanner.nextLine());

        System.out.print("Enter Marks in Subject 1: ");
        int marks1 = scanner.nextInt();

        System.out.print("Enter Marks in Subject 2: ");
        int marks2 = scanner.nextInt();

        System.out.print("Enter Marks in Subject 3: ");
        int marks3 = scanner.nextInt();

        // Set the marks for the student
        result.setMarks(marks1, marks2, marks3);

        // Display the result
        result.displayResult();

        scanner.close();
    }
}
```

# 15. Polymorphism with Shape Area Calculation.

```java
import java.util.Scanner;

// Base class Shape
abstract class Shape {
    abstract double calculateArea();
}

// Derived class Circle
class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    @Override
    double calculateArea() {
        return 3.14159 * radius * radius;
    }
}

// Derived class Rectangle
class Rectangle extends Shape {
    private double length;
    private double breadth;

    public Rectangle(double length, double breadth) {
        this.length = length;
        this.breadth = breadth;
    }

    @Override
    double calculateArea() {
        return length * breadth;
    }
}

// Derived class Triangle
class Triangle extends Shape {
    private double base;
    private double height;

    public Triangle(double base, double height) {
        this.base = base;
        this.height = height;
    }

    @Override
    double calculateArea() {
        return 0.5 * base * height;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Accept input for Circle
        System.out.print("Enter the radius of the circle: ");
        double radius = scanner.nextDouble();
        Shape circle = new Circle(radius);

        // Accept input for Rectangle
        System.out.print("Enter the length of the rectangle: ");
        double length = scanner.nextDouble();
        System.out.print("Enter the breadth of the rectangle: ");
        double breadth = scanner.nextDouble();
        Shape rectangle = new Rectangle(length, breadth);

        // Accept input for Triangle
        System.out.print("Enter the base of the triangle: ");
        double base = scanner.nextDouble();
        System.out.print("Enter the height of the triangle: ");
        double height = scanner.nextDouble();
        Shape triangle = new Triangle(base, height);

        // Display the areas of all shapes
        System.out.println("Area of the circle: " + String.format("%.2f", circle.calculateArea()));
        System.out.println("Area of the rectangle: " + String.format("%.2f", rectangle.calculateArea()));
        System.out.println("Area of the triangle: " + String.format("%.2f", triangle.calculateArea()));

        scanner.close();
    }
}
```

# 16. Implementing Polymorphism for Shape Hierarchies.

```java
import java.util.Scanner;

abstract class Shape {
    // Abstract method for calculating area
    public abstract double calculateArea();
}

class Circle extends Shape {
    private double radius;

    // Constructor to initialize the radius
    public Circle(double radius) {
        this.radius = radius;
    }

    // Overridden method to calculate the area of the circle
    @Override
    public double calculateArea() {
        return 3.14159 * radius * radius;
    }
}

class Rectangle extends Shape {
    private double length, breadth;

    // Constructor to initialize length and breadth
    public Rectangle(double length, double breadth) {
        this.length = length;
        this.breadth = breadth;
    }

    // Overridden method to calculate the area of the rectangle
    @Override
    public double calculateArea() {
        return length * breadth;
    }
}

class Triangle extends Shape {
    private double base, height;

    // Constructor to initialize base and height
    public Triangle(double base, double height) {
        this.base = base;
        this.height = height;
    }

    // Overridden method to calculate the area of the triangle
    @Override
    public double calculateArea() {
        return 0.5 * base * height;
    }
}

public class ShapeAreaCalculation {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Accept user input for each shape
        System.out.print("Enter the radius of the circle: ");
        double radius = scanner.nextDouble();
        Shape circle = new Circle(radius);

        System.out.print("Enter the length of the rectangle: ");
        double length = scanner.nextDouble();
        System.out.print("Enter the breadth of the rectangle: ");
        double breadth = scanner.nextDouble();
        Shape rectangle = new Rectangle(length, breadth);

        System.out.print("Enter the base of the triangle: ");
        double base = scanner.nextDouble();
        System.out.print("Enter the height of the triangle: ");
        double height = scanner.nextDouble();
        Shape triangle = new Triangle(base, height);

        // Displaying the area of each shape using polymorphism
        System.out.println("Area of the circle: " + circle.calculateArea());
        System.out.println("Area of the rectangle: " + rectangle.calculateArea());
        System.out.println("Area of the triangle: " + triangle.calculateArea());

        scanner.close();
    }
}
```

# 17. Matrix Multiplication Using Function Overloading

```java
import java.util.Scanner;

public class MatrixOperations {

    // Function to perform matrix addition
    public static void operate(int[][] A, int[][] B) {
        int m = A.length;
        int n = A[0].length;
        int p = B.length;
        int q = B[0].length;

        // Check if dimensions are the same for matrix addition
        if (m != p || n != q) {
            System.out.println("Invalid dimensions for operation.");
            return;
        }

        int[][] result = new int[m][n];

        // Perform matrix addition
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                result[i][j] = A[i][j] + B[i][j];
            }
        }

        // Print the result of matrix addition
        System.out.println("Matrix Addition Result:");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }
    }

    // Function to perform matrix multiplication
    public static void operate(int[][] A, int[][] B, int m, int n, int p) {
        int q = B[0].length;

        // Check if matrix multiplication dimensions are valid
        if (n != B.length) {
            System.out.println("Invalid dimensions for operation.");
            return;
        }

        int[][] result = new int[m][q];

        // Perform matrix multiplication
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < q; j++) {
                result[i][j] = 0;
                for (int k = 0; k < n; k++) {
                    result[i][j] += A[i][k] * B[k][j];
                }
            }
        }

        // Print the result of matrix multiplication
        System.out.println("Matrix Multiplication Result:");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < q; j++) {
                System.out.print(result[i][j] + " ");
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input dimensions for matrix A
        System.out.print("Enter the number of rows and columns for Matrix A (m x n): ");
        int m = scanner.nextInt();
        int n = scanner.nextInt();

        // Input dimensions for matrix B
        System.out.print("Enter the number of rows and columns for Matrix B (n x p): ");
        int p = scanner.nextInt();
        int q = scanner.nextInt();

        // Initialize matrix A and B
        int[][] A = new int[m][n];
        int[][] B = new int[p][q];

        // Input elements for matrix A
        System.out.println("Enter the elements of Matrix A:");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                A[i][j] = scanner.nextInt();
            }
        }

        // Input elements for matrix B
        System.out.println("Enter the elements of Matrix B:");
        for (int i = 0; i < p; i++) {
            for (int j = 0; j < q; j++) {
                B[i][j] = scanner.nextInt();
            }
        }

        // Input for operation type
        System.out.print("Enter operation type (1 for Addition, 2 for Multiplication): ");
        int operation = scanner.nextInt();

        // Perform the chosen operation
        if (operation == 1) {
            operate(A, B);
        } else if (operation == 2) {
            operate(A, B, m, n, p);
        } else {
            System.out.println("Invalid operation.");
        }

        scanner.close();
    }
}
```


# 18. Polymorphism in Shape Classes

```java
import java.util.Scanner;

abstract class Shape {
    // Abstract method to calculate the area
    public abstract double getArea();
}

class Rectangle extends Shape {
    private double length;
    private double breadth;

    // Constructor to initialize dimensions
    public Rectangle(double length, double breadth) {
        this.length = length;
        this.breadth = breadth;
    }

    // Override getArea for rectangle
    @Override
    public double getArea() {
        return length * breadth;
    }
}

class Circle extends Shape {
    private double radius;

    // Constructor to initialize radius
    public Circle(double radius) {
        this.radius = radius;
    }

    // Override getArea for circle
    @Override
    public double getArea() {
        return Math.PI * radius * radius;
    }
}

class Triangle extends Shape {
    private double base;
    private double height;

    // Constructor to initialize base and height
    public Triangle(double base, double height) {
        this.base = base;
        this.height = height;
    }

    // Override getArea for triangle
    @Override
    public double getArea() {
        return 0.5 * base * height;
    }
}

public class ShapeAreaCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter shape type (1 for Rectangle, 2 for Circle, 3 for Triangle): ");
        int shapeType = scanner.nextInt();

        Shape shape = null;

        switch (shapeType) {
            case 1:
                System.out.print("Enter length and breadth for Rectangle: ");
                double length = scanner.nextDouble();
                double breadth = scanner.nextDouble();
                shape = new Rectangle(length, breadth);
                break;
            case 2:
                System.out.print("Enter radius for Circle: ");
                double radius = scanner.nextDouble();
                shape = new Circle(radius);
                break;
            case 3:
                System.out.print("Enter base and height for Triangle: ");
                double base = scanner.nextDouble();
                double height = scanner.nextDouble();
                shape = new Triangle(base, height);
                break;
            default:
                System.out.println("Invalid shape type.");
                return;
        }

        System.out.println("Area of the shape: " + shape.getArea());
        scanner.close();
    }
}
```


# 19. Implement Multiple Inheritance to Simulate a Library System

```java
import java.util.Scanner;

// Interface for Book
interface Book {
    String getTitle();
    String getAuthor();
    int getISBN();
}

// Interface for Borrower
interface Borrower {
    String getName();
    int getID();
}

// Class Library that implements both Book and Borrower interfaces
class Library implements Book, Borrower {
    private String title;
    private String author;
    private int isbn;
    private String borrowerName;
    private int borrowerID;
    private boolean isBookBorrowed;

    // Constructor to initialize book and borrower details
    public Library(String title, String author, int isbn, String borrowerName, int borrowerID) {
        this.title = title;
        this.author = author;
        this.isbn = isbn;
        this.borrowerName = borrowerName;
        this.borrowerID = borrowerID;
        this.isBookBorrowed = false;  // Initially, the book is not borrowed
    }

    // Implement Book interface methods
    @Override
    public String getTitle() {
        return title;
    }

    @Override
    public String getAuthor() {
        return author;
    }

    @Override
    public int getISBN() {
        return isbn;
    }

    // Implement Borrower interface methods
    @Override
    public String getName() {
        return borrowerName;
    }

    @Override
    public int getID() {
        return borrowerID;
    }

    // Method to borrow the book
    public void borrowBook() {
        if (isBookBorrowed) {
            System.out.println("The book is already borrowed.");
        } else {
            isBookBorrowed = true;
            System.out.println("Book borrowed by " + borrowerName + " (ID: " + borrowerID + ")");
        }
    }

    // Method to return the book
    public void returnBook() {
        if (!isBookBorrowed) {
            System.out.println("The book is not borrowed.");
        } else {
            isBookBorrowed = false;
            System.out.println("Book returned by " + borrowerName + " (ID: " + borrowerID + ")");
        }
    }
}

public class LibrarySystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input book details
        System.out.println("Enter Book Title: ");
        String title = scanner.nextLine();
        System.out.println("Enter Book Author: ");
        String author = scanner.nextLine();
        System.out.println("Enter Book ISBN: ");
        int isbn = scanner.nextInt();

        // Input borrower details
        scanner.nextLine();  // Consume newline left by nextInt()
        System.out.println("Enter Borrower Name: ");
        String borrowerName = scanner.nextLine();
        System.out.println("Enter Borrower ID: ");
        int borrowerID = scanner.nextInt();

        // Create a Library object with the details
        Library library = new Library(title, author, isbn, borrowerName, borrowerID);

        // Menu for actions
        System.out.println("Choose Action: ");
        System.out.println("1. Borrow a Book");
        System.out.println("2. Return a Book");

        int action = scanner.nextInt();

        // Perform action based on user input
        switch (action) {
            case 1:
                library.borrowBook();
                break;
            case 2:
                library.returnBook();
                break;
            default:
                System.out.println("Invalid action.");
                break;
        }

        scanner.close();
    }
}
```


# 20. Implement Polymorphism for Banking Transactions

```java
import java.util.Scanner;

// Base class: Account
abstract class Account {
    protected double balance;

    // Constructor to initialize balance
    public Account(double balance) {
        this.balance = balance;
    }

    // Abstract method to calculate interest or fees (to be overridden in derived classes)
    public abstract void calculateInterest();
}

// Derived class: SavingsAccount
class SavingsAccount extends Account {
    private double interestRate;
    private int time;

    // Constructor to initialize balance, interest rate, and time
    public SavingsAccount(double balance, double interestRate, int time) {
        super(balance);
        this.interestRate = interestRate;
        this.time = time;
    }

    // Override the calculateInterest method
    @Override
    public void calculateInterest() {
        double interest = (balance * interestRate * time) / 100;
        System.out.println("Savings Account Interest: " + interest);
    }
}

// Derived class: CurrentAccount
class CurrentAccount extends Account {
    private double maintenanceFee;

    // Constructor to initialize balance and maintenance fee
    public CurrentAccount(double balance, double maintenanceFee) {
        super(balance);
        this.maintenanceFee = maintenanceFee;
    }

    // Override the calculateInterest method
    @Override
    public void calculateInterest() {
        // No interest for current account, but we subtract maintenance fee
        balance -= maintenanceFee;
        System.out.println("Current Account Maintenance Fee Deduction: " + maintenanceFee);
        System.out.println("Remaining Balance after Fee: " + balance);
    }
}

public class BankingSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter Account Type (1 for Savings, 2 for Current): ");
        int accountType = scanner.nextInt();

        System.out.print("Enter Account Balance: ");
        double balance = scanner.nextDouble();

        Account account = null;

        if (accountType == 1) {
            System.out.print("Enter Interest Rate (%): ");
            double interestRate = scanner.nextDouble();
            System.out.print("Enter Time (in years): ");
            int time = scanner.nextInt();
            account = new SavingsAccount(balance, interestRate, time);
        } else if (accountType == 2) {
            System.out.print("Enter Monthly Maintenance Fee: ");
            double maintenanceFee = scanner.nextDouble();
            account = new CurrentAccount(balance, maintenanceFee);
        } else {
            System.out.println("Invalid account type");
            return;
        }

        account.calculateInterest();
        scanner.close();
    }
}
```
