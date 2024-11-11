Problems often contain some conditional logic. In these instances we use conditional statements. A conditional statement starts with an `if` command followed by an expression in parentheses. The expression evaluates to either true or false. If it evaluates true, the following block delimited by curly brackets gets executed.

```java
// if the value is greater than five
if (value > 5) {
    // then...
}
```

A program that prints "ok" if the value of the variable is greater than `42`, and otherwise prints "not ok" looks like this:

```java
int value = 15;
if (value > 42) {
    System.out.println("ok");
} else {
    System.out.println("not ok")
}
```

You can also chain together multiple conditions. In such a case, the problem takes the form "if a, then b; else if c, then d; else if e, then f; otherwise g". The chain consists of an `if`-statement followed by `else if`-statements, each containing its own expression and a block.

```java
// if the value is greater than five
if (value > 5) {
    // functionality when value is greater than five
} else if (value < 0) { //
    // functionality when value is less than zero
    // and the value IS NOT larger than five
} else {  // otherwise
    // functionality otherwise
}
```

Conditional logic can be combined with other patterns used for problem solving. Let's look into a problem "Read two integers from the user. If the sum of the integers is over 100, print `too much`. If the sum is less than 0, print `too little`. Otherwise, print `ok`. The program below combines reading, calculating and conditional functionality.

```java
// Bringing Scanner to the program's use
import java.util.Scanner;

public class Program {
    public static void main(String[] main) {
        // Creating the scanner
        Scanner reader = new Scanner(System.in);

        // Declaring the variables and assigning user input to them
        int first = Integer.valueOf(reader.nextLine());
        int second = Integer.valueOf(reader.nextLine());

        // Identifying the operation and declaring variable for the result
        int sum = first + second;

        // Doing something with the result. In this case
        // the result is used in the conditional operations.

        if (sum > 100) { // if the sum is over 100
            System.out.println("too much");
        } else if (sum < 0) { // if the sum is less than 0
            System.out.println("too little");
        } else { // otherwise
            System.out.println("ok");
        }
    }
}
```