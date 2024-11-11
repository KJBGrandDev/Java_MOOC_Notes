### Learning Objectives

- You are familiar with loops and know how to create a program that contains one.

- You know how to use the `break` command to end a loop's execution.

- You know how to use `continue` command to return to the beginning of a loop.

- You are able to create a program that reads inputs from a user until a specific input is given. For example, the number 0 or the string "end", after which the program prints something about the provided inputs (e.g., the input count, and in the case of numbers their sum and average).

A computer's processor, which specializes in executing commands, is capable of executing — in a modern computer — over a billion (machine code) commands in a second.

In this section, we'll get used to writing often-repeated program code with the help of loops.

Let's motivate ourselves to use loops. Below you'll find an example of a program that asks the user for five numbers and calculates their sum.

```java
Scanner scanner = new Scanner(System.in);
int sum = 0;

System.out.println("Input a number: ");
sum = sum + Integer.valueOf(scanner.nextLine());

System.out.println("Input a number: ");
sum = sum + Integer.valueOf(scanner.nextLine());

System.out.println("Input a number: ");
sum = sum + Integer.valueOf(scanner.nextLine());

System.out.println("Input a number: ");
sum = sum + Integer.valueOf(scanner.nextLine());

System.out.println("Input a number: ");
sum = sum + Integer.valueOf(scanner.nextLine());

System.out.println("The sum of the numbers is " + sum);
```

It does the job, but not elegantly. What if the program had to read a hundred, or perhaps a thousand numbers and print their sum? What if the program had to read three numbers only?

The problem can be solved with a loop which keeps track of both the sum and the number of times input has been read. The program that prints the sum of five numbers now looks as follows

```Java
import java.util.Scanner

public class Program{
	public static void main(String[] args)
}
```

Next off we will get familiar with loops.