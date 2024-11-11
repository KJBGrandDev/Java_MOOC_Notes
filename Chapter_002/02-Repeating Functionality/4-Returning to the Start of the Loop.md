When the execution reaches the end of the loop, the execution starts again from the start of the loop. This means that all the commands in the loop have been executed. You can also return to the beginning from other places besides the end with the command `continue`. When the computer executes the command `continue`, the execution of the program moves to the beginning of the loop.

The example below demonstrates the use of the `continue` command. The program asks the user to input positive numbers. If the user inputs a negative number or a zero, the program prints the message "Unfit number, try again", after which the execution returns to the beginning of the loop. In the previous example, the program read inputs of type string from the user. Similar programs with different input types are also possible. In the example below, the user is asked for numbers until they input a zero.

```Java
import java.util.Scanner;

public class Program{
	public static void main(String[] args){
		Scanner scanner = new Scanner(System.in);

	while(true){
		System.out.println("Insert positive integers");
		int number = Integer.valueOf(scanner.nextLine());

		if (number <= 0) {
			System.out.println("Unfit number! Try Again.");
			continue;
		}
		System.out.println("Your input was " + number);
		}
	}
}
```

The program in the example above is repeated infinitely since the `break` command used for exiting the loop is not used. To exit the loop, the `break` command must be added to it.

In the example below, the program is modified in such a way that the user is asked to input positive numbers. If the user inputs a negative number, the program informs them that the number was unfit and returns to the beginning of the loop. If the number was zero, the program exits the loop.

```java
Scanner scanner = new Scanner(System.in);

while (true) {
    System.out.println("Input positive numbers.");
    int number = Integer.valueOf(scanner.nextLine());

    if (number == 0) {
        break;
    }

    if (number < 0) {
        System.out.println("Unfit number! Try again.");
        continue;
    }

    System.out.println("Your input was " + number);
}
```

Quiz:

## Exiting loop and limit

What does the program below print?

```Java
public static void main(String[] args) {
    int number = 0;

    while (true) {
        number = number + 1;

        if (number >= 5) {
            break;
        }

        if (number < 5) {
            continue;
        }

        System.out.print(number + " ");
    }

    System.out.print(number + " ");
}
//Result
1 2 3 4 5
```

![[Pasted image 20240906232625.png]]

In the previous exercise, you made a program that asks the user for numbers. If the user entered a negative number, the program would inform them that the number was unfit, and if the user entered a zero, the program would exit. A possible solution to the exercise is the following.

```java
Scanner scanner = new Scanner(System.in);

while (true) {
    System.out.println("Input a number");
    int number = Integer.valueOf(scanner.nextLine());

    if (number == 0) {
        break;
    }

    if (number < 0) {
        System.out.println("Unfit number");
        continue;
    }

    System.out.println(number * number);
}
```

The program could be made by modifying the if-statement to another form. In the example below, the conditionals have been combined to replace separate if-statements.

```java
Scanner scanner = new Scanner(System.in);

while (true) {
    System.out.println("Input a number");
    int number = Integer.valueOf(scanner.nextLine());

    if (number == 0) {
        break;
    } else if (number < 0) {
        System.out.println("Unfit number");
        continue;
    }

    System.out.println(number * number);
}
```

Which of the previous examples was more clear?

Let's examine the clarity of the previous programs through an example. Below, the program asks the user for a number. If the number is negative, the user is informed that the number is unfit and the execution of the program goes to the beginning of the loop. If the number is zero, the program exits the loop. In other cases the program prints the square of the number, i.e., the number times itself.

```java
Scanner scanner = new Scanner(System.in);

while (true) {
    System.out.println("Input a number ");
    int number = Integer.valueOf(scanner.nextLine());

    if (number < 0) {
        System.out.println("Unfit number");
        continue;
    }

    if (number == 0) {
        break;
    }

    System.out.println(number * number);
}
```

This program can also be done by combining the if-statements. In that case, the implementations would be the following.

```java
Scanner scanner = new Scanner(System.in);

while (true) {
    System.out.println("Input a number ");
    int number = Integer.valueOf(scanner.nextLine());

    if (number < 0) {
        System.out.println("Unfit number");
    } else if (number == 0) {
        break;
    } else {
        System.out.println(number * number);
    }
}
```

Let's examine the previous programs with comments. Before each command, there's a comment that aims to explain what's happening in the program. Below is a program that's written with separate if-statements.

```java
// The task is to read an input from the user
Scanner scanner = new Scanner(System.in);

// The task is to repeat the block until the block is exited
while (true) {
    // The task is to ask the user for an input
    System.out.println("Input a number ");
    // The task is to read a number from the user
    int number = Integer.valueOf(scanner.nextLine());

    // The task is to guard and prevent unfit numbers
    // for further processing
    if (number < 0) {
        System.out.println("Unfit number");
        continue;
    }

    // The task is to check if the loop should be exited
    if (number == 0) {
        break;
    }

    // The task is to print the square of the number
    System.out.println(number * number);
}
```

Note that every if-statement has a single, clear task.

When we comment on a program containing combined if-statements, the comments take the following form.

```java
// The task is to read an input from the user
Scanner scanner = new Scanner(System.in);

// The task is to repeat the block until the block is exited
while (true) {
    // The task is to ask the user for an input
    System.out.println("Input a number ");
    // The task is to read a number from the user
    int number = Integer.valueOf(scanner.nextLine());

    // The purpose of the if-else if-else block?
    // The task is the processing of the number?
    if (number < 0) {
        System.out.println("Unfit number");
    } else if (number == 0) {
        break;
    } else {
        System.out.println(number * number);
    }
}
```

We notice that it's difficult to define a single, clear task for `if-else if-else`-block. **During the design and implementation of a program, it's desirable to aim for a situation in which every part of the program has a a single, clear task.** This theme repeats throughout the course.

