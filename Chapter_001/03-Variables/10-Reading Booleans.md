The "Integer.valueOf" command converts a string to an integer and the "Double.valueOf" converts it to a floating-point. The "valueOf" command also appears when converting a string to a boolean - this is done with the command "Boolean.valueOf".

Boolean variables can either have the value of true or false. When converting a string into a boolean, the string must be "true" if we want the boolean value to be "true". The case is insensitive here: both "true" and "TRue" can turn into the boolean value of "true". All other strings turn into the boolean "false".

```Java
import java.util.Scanner;

public class Program{
	public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);
	System.out.println("Write a boolean ");
	boolean value = Boolean.valueOf(scanner.nextLine());
	System.out.println("You wrote " + value);
	}
}
```

```Java
Write a boolean
I wont!
You wrote false
```

```Java
Write a boolean
TRUE
You wrote true
```

```Java
Write a boolean
true
You wrote true
```