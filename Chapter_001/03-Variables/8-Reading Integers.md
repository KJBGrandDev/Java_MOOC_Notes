The "Integer.valueOf" command converts a string into an integer. It takes the string containing the value to be converted as a parameter.
```Java
String valueAsString = "42";
int value = Integer.valueOf(valueAsString);

System.out.println(value); //42
```

When using a scanner object, the reading of the value is usually inserted directly into the type conversion. This happens like so:
```Java
import java.util.Scanner;

public class Program{
	public class static void(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Write a value: ");
	int value = Integer.valueOf(scanner.nextLine());
	System.out.println("You wrote " + value);
	}
}
```