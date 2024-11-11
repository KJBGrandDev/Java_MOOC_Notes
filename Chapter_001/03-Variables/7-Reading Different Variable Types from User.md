In the text-based user interfaces that we've used in our programs, the user's input is always read as a string, since the user writes their input as text. Reading strings from the user has become familiar by this point - we do it using the "nextLine" command of the Scanner helper method.
```Java
import java.util.scanner;

public class Program{
	public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Write text and press enter ");
	String text = scanner.nextLine();
	System.out.println("You wrote " + text);
	}
}
```

Other input types, such as integers, doubles, and booleans, are also read as text. However, they need to be converted to the target variable's type with the help of some tools provided by Java.