<mark class="hltr-purple">Input</mark> <mark class="hltr-yellow">refers to text written by the user</mark> **read by the program**.

<mark class="hltr-purple">Input</mark> is always **"read" as "string"**.

For reading input, we use the "Scanner" tool that comes with Java. 
The tool can be imported for use in program by adding the command "import java.util.Scanner;" before the beginning of the main's program's frame (public class...) The tool itself is created with Scanner scanner = new Scanner(System.in);
```Java
import java.util.Scanner

public class Program{
	public static main void(String[] args){
	Scanner scanner = new Scanner(System.in);

	//We can now use the Scanner tool.
	//This tool is used to read input.
	}
}
```

Program which asks for user input, reads the string entered by the user, and then prints it.
```Java
//Introduce the scanner tool used for reading user input.
import java.util.Scanner;

public class Dinosaur {

    public static void main(String[] args) {

        //Create a tool for reading user input and name it scanner
        Scanner scanner = new Scanner(System.in);

        //Print "Write a Message: "
        System.out.println("Write a message: ");

        //Read the string written by the user, and assign it
        //to program memory "String message = (string that was given as input)".
        String message = scanner.nextLine();

        //Print the message written by the user
        System.out.println(message);
    }
}
```

More precisely, input is read with "scanner" tool's "nextLine()" method.
The call "scanner.nextLine()" is left waiting for the user to write something. When user writes something and presses enter, the provided string is assigned to a "string variable" (in this instance, variable "message").

The program is then able to reference the variable "message" later on.. In the example above, the variable "message" is referenced in the "print" command.

When the program is run, its output can look like the example below
```Java
Write a message :
Hello World //User input
Hello World //Variable message called by print command
```