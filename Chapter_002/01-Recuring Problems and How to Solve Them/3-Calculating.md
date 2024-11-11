We quite often need to calculate something in a program, such as an average or a sum. The solution pattern to solve such problems is as follows.

1. Define the inputs required for the calculation and declare variables for them. Input refers to the values used in the calculation. You can typically identify the type of inputs from the problem description.
2. Identify the operation needed, and declare a variable for the result of the calculation. Perform the calculation using the inputs, and assign the result to the variable that was reserved for it. The type of the result can also usually be identified from the problem description.
3. Once the calculation is done, do something with its result. This can mean printing the result of a computation, or, for example, using it in calculating an average by dividing a sum of the inputs by their count.

For example, the solution pattern for the problem _Create a program to calculate the sum of two integers_ is the following.

```Java
// Identifying the input values and declaring the variables for them
int first = 1;
int second = 2;

// Identifying the operation and declaring a variable for the result
int sum = first + second;

// Printing the result of the calculation
System.out.println("The sum of " + first + " and " + second + " is " + sum);
```

A program that both reads and calculates combines both of these patterns. One that calculates the product of two integers provided by the user looks like this:

```java
// Making the scanner available in the program
import java.util.Scanner;

public class Program {
    public static void main(String[] main) {
        // Creating the scanner
        Scanner reader = new Scanner(System.in);

        // Identifying the input values and declaring the variables for them
        int first = 1;
        int second = 2;

        // Assigning the user input to the variables
        first = Integer.valueOf(reader.nextLine());
        second = Integer.valueOf(reader.nextLine());

        // Identifying the operation and declaring a variable for the result
        int product = first * second;

        // Printing the result of the operation
        System.out.println("The product of " + first + " and " + second + " is " + product);

    }
}
```

In the example above, the program has been implemented so that the variables are declared first after which values are read into them. Variable declaration and the reading of values into them can also be combined into one.

```java
// Making the Scanner available to the program
import java.util.Scanner;

public class Program {
    public static void main(String[] main) {
        // Creating the Scanner
        Scanner reader = new Scanner(System.in);

        // Declaring the variables and assigning user input to them
        int first = Integer.valueOf(reader.nextLine());
        int second = Integer.valueOf(reader.nextLine());

        // Identifying the operation and declaring a variable for the result
        int product = first * second;

        // Printing the result of the operation
        System.out.println("The product of " + first + " and " + second + " is " + product);

    }
}
```

Method to get a Square Root:

```Java
import java.util.Scanner;

public class SquareRootOfSum {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int first = Integer.valueOf(scanner.nextLine());
        int second = Integer.valueOf(scanner.nextLine());

        int sum = first + second;
        double squareRoot = Math.sqrt(sum);

        System.out.println(squareRoot);
    }
}
```