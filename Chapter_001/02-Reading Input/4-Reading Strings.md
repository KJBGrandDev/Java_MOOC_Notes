The "reader.nextLine();" command reads the user's input and "returns" a string.

If we then want to use the string in the program, it must be saved to a string variable.
```Java
String message = scanner.nextLine();
```

A value saved to a variable can be used repeatedly

In the example below, the user input is printed twice:
```Java
//Introduce the Scanner tool for reading
import java.util.Scanner

public class Program{
	public static void main(String[] args){
	//Create the tool for reading, assign it to a variable called scanner
	Scanner scanner = new Scanner(System.in);

	//Print user a message "Write a message"
	System.out.println("Write a message: ");

	//Read the user's string input, save it to program memory
	//String message = (user input)
	String message = scanner.nextLine();

	//Print the user input twice
	System.out.println(message);
	System.out.println(message);
	}
}
```