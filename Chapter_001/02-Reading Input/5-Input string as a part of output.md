We noticed in the "Hi Ada Lovelace!" exercise that string literals and string variables can be joined using the " + " operator.

The example below demonstrates a program that takes user input and prints it "concatenated" with a string literal.
```Java
import java.util.Scanner

public class Program{
	public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Write a message: ");

	String message = scanner.nextLine();

	System.out.println("You wrote " + message);
	}
}
```