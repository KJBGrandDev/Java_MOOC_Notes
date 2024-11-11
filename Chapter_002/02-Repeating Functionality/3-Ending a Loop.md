The loop can be broken out of with command 'break'. When a computer executes the command 'break', the program execution moves onto the next command following the loop block.

The example below is a program that prints numbers from one to five. Note how the variable that's used within the loop is defined before the loop. This way the variable can be incremented inside the loop and the change sticks between multiple iterations of the loop.

```Java
public class Program{
	public static void main(String[] args){
		int number = 1;

	while (true){
		System.out.println(number);
		if(number >= 5){
			break;
		}
		number = number += 1;
	}
	System.println("Ready!");
	}
}
// Results
1
2
3
4
5
Ready!
```

Breaking out of the loop occurs when a user enters a specified input or whenever a calculation performed in the loop ends in the desired result. These kinds of programs contain both a loop used to define a section to be repeated and also a conditional expression used to check whether or not the condition to exit the loop has been fulfilled.

Users can also be asked for input within a loop. The variables that are commonly used in loops (such as Scanner readers) are defined before the loop, whereas variables (such as the value read from the user) that are specific to the loop are defined within it.

In the example below, the program asks the user whether to exit the loop or not. If the user inputs the string "y", the execution of the program moves to the command following the loop block, after which the execution of the program ends.

```Java
import java.util.Scanner;

public class Program{
	public static void main(String[] args){
		Scanner scanner = new Scanner(System.in);

	while(true){
		System.out.println("Exit? (y exits)");
		String input = scanner(nextLine());
		if(input.equals("y")){
			break;
		}
		System.out.println("Ok! Let's carry on!");
	}
	System.out.println("Ready!");
	}
}
// Results
Exit? (y exits)
no
Ok! Let's carry on!
Exit? (y exits)
non
Ok! Let's carry on!
Exit? (y exits)
y
Ready!
```

In the previous example, the program read inputs of type string from the user. The program can also be implemented with other types of variables. The program below asks numbers from the user until the user inputs a zero.

```Java
import java.util.Scanner;

public class Program{
	public static void main(String[] args){
		Scanner scanner = new Scanner(System.in);

	while(true){
		System.out.println("Input a number, 0 to quit");
		int command = Integer.valueOf(scanner.nextLine());
		if (command == 0){
			break;
		}
		System.out.println("You input " + command);
	}
	System.out.println("Done, thank you!");
	}
}
```

The output of the program can be as follows:

```Java
Input a number, 0 to quit 
5 
You input 5 
Input a number, 0 to quit 
-2 
You input -2 
Input a number, 0 to quit 
0
Done, thank you!
```