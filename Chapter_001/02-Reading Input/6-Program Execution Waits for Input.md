When the program's execution comes a statement that attempts to read input from the user (the command "reader.nextLine()"), the execution stops and waits.

The execution continues only after the user has written some input and pressed "enter".

In the example below, the program prompts the user for "Three strings". First the program prints "Write the first string: ", and then waits for user input.

When the user writes some text, the program prints "Write the second string: ", and then waits for user input again.

This continues for a third time, after which the program prints all three strings.
```Java
import java.util.Scanner

public class Program{
	public class static void(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Write the first string: ");
	String first = scanner.nextLine();
	System.out.println("Write the second string: ");
	String second = scanner.nextLine();
	System.out.println("Write the third string: ");
	String third = scanner.nextLine();

	System.out.println("You wrote: ");
	System.out.println(first);
	System.out.println(second);
	System.out.println(third);
	}
}
```

In the previous example, we saved the user input to three different string variables. This can be done as long as the variables all have different names(in the example, the names are first, second, and third)

We can form complicated texts whose content changes depending on the user's input by using more strings. In the example below, the user is told a bit more about the texts they wrote - notice that the order in which the strings are printed can be changed.

In the example below, the third input is printed first.
```Java
import java.util.Scanner

public class Program{
	public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Write the first string: ");
	String first = scanner.nextLine();
	System.out.println("Write the second string: ");
	String second = scanner.nextLine();
	System.out println("Write the third string: ");
	String third = scanner.nextLine();

	System.out.println("Last string you wrote was " + third + ", which");
	System.out.println("was preceded by " + second + ".");
	System.out.println("The first string was " + first ".");

	System.out.println("All together: " + first + second + third);
	}
}
```