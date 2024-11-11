The "Double.valueOf" converts a string to a double. It takes the string containing the value to be converted as a parameter.
```Java
String valueAsString = "42.42";
double value = Double.valueOf(valueAsString);
System.out.println(value); //42.42
```

As with integers, the reading is nested within the conversion. This is done as follows:
```Java
import java.util.Scanner;

public class Program{
	public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);
	System.out.println("Write a value: ");
	double value = Double.valueOf(scanner.nextLine());
	System.out.println("You wrote " + value);
	}
}
```

It's possible to also read an integer variable into a double, in which case the value is converted automatically to type double. The example below demonstrates how the previous program functions when the user inputs an integer.
```Java
Write a value
18
You wrote 18.0
```