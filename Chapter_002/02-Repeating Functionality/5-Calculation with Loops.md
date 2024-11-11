Loops are used in computing many different things. For example, programs that process indefinite numbers of user-inputted values make use of loops. These kinds of programs typically print out some sort of statistics about the numbers that were read or other inputs after the end loop.

For the program to print out information from the loop execution after the loop, the information must be saved and modified during the loop.

If the variable used to store the data is introduced within the loop, the variable is only available within that loop and nowhere else.

Let's create a program to count and print out the number of ones entered by the user. Let's first create a non-working version and examine the action of the blocks.

```Java
public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);

	while(true){
		// The task is to keep count of number ones
		int ones = 0;
		
		System.out.println("Input a number (0 exits));
		// The task is to read a user inputted number
		int number = Integer.valueOf(scanner.nextLine());
		
		// The task is to exit the loop if the user
		// has inputted a zero
		if(number === 0){
			break;
		}
		// The task is to increase the amount of ones
		// If the user inputs a number one
		if(number === 1){
			ones = ones + 1;
		}
	}
	System.out.println("The total of ones: " + ones);
}
```

The previous program does not work because the variable `ones` is introduced within the loop, and an attempt is made to use it after the loop at the end of the program. The variable only exists inside the loop. If the print statement `System.out.println("The total of ones: " + ones);` was inside the loop, the program would work, but not in the desired way. Let's examine this next.

```java
Scanner scanner = new Scanner(System.in);

// The task is to read an input from the user
while (true) {

    // The task is to keep count of number ones
    int ones = 0;

    System.out.println("Insert a number (0 exits): ");
    // The task is to read a user inputted number
    int number = Integer.valueOf(scanner.nextLine());

    // The task is to exit the loop if the user
    // has inputted zero
    if (number == 0) {
        break;
    }

    // The task is to increase the amount of ones
    // if the user inputs a number one
    if (number == 1) {
        ones = ones + 1;
    }

    // The task is to print out the total of ones
    System.out.println("The total of ones: " + ones);
}
```

The example above works, but not in a way we hoped it would. Below the example output of the program

```Java
Insert a number (0 exits) 
5
The total of ones: 0 
Insert a number (0 exits) 
1
The total of ones: 1 
Insert a number (0 exits) 
1
The total of ones: 1 
Insert a number (0 exits) 
2
The total of ones: 0 
Insert a number (0 exits) 
0
```

If you wish to use a variable after a loop, it needs to be introduced before the loop.

In the example below, the program computes the total of number ones inputted. The inputs are read until the user inputs a zero after which the program prints the total count of number ones entered. The program uses variable `ones` to keep track of the number ones.

```java
Scanner scanner = new Scanner(System.in);

// The task is to keep track of number ones
int ones = 0;

// The task is to read an input from the user
while (true) {
    System.out.println("Give a number (end with 0): ");
    // The task is to read a user inputted number
    int number = Integer.valueOf(scanner.nextLine());

    // The task is to exit the loop if the user
    // has inputted zero
    if (number == 0) {
        break;
    }

    // The task is to increase the amount of ones
    // if the user inputs a number one
    if (number == 1) {
        ones = ones + 1;
    }
}

// The task is to print out the total of ones
System.out.println("The total of ones: " + ones);
```

Below is an example output of the program.

```Java
Give a number (end with 0): 
1
Give a number (end with 0): 
2
Give a number (end with 0): 
1
Give a number (end with 0): 
-1
Give a number (end with 0): 
0
Total of ones: 2
```

![[Pasted image 20240907175606.png]]

![[Pasted image 20240907175633.png]]

The programs written in the previous exercises have read input from the user and kept track of the count of certain types of numbers. In the next exercise, the requested sum of numbers is not much different — this time, rather than keeping track of the number of values entered, you add the number entered by the user to the sum.

![[Pasted image 20240907180047.png]]

Sometimes you need to use multiple variables. The example below shows a program which reads numbers from the user until the user writes 0. Then the program prints the number of positive and negative numbers given, and the percentage of positive numbers from all numbers given.

```java
Scanner reader = new Scanner(System.in);

// For saving number of numbers
int numberOfPositives = 0;
int numberOfNegatives = 0;

// For repeatedly asking for numbers
while (true) {
    System.out.println("Give a number (0 to stop): ");
    // For reading user input
    int numberFromUser = Integer.valueOf(reader.nextLine());

    // For breaking the loop when user writes 0
    if (numberFromUser == 0) {
        break;
    }

    // For increasing numberOfPositives by one
    // when user gives a positive number
    if (numberFromUser > 0) {
        numberOfPositives = numberOfPositives + 1;
    }

    // For increasing numberOfNegatives by one
    // when user gives a negative number
    if (numberFromUser < 0) {
        numberOfNegatives = numberOfNegatives + 1;
    }

    // Also could have used..
    // if (numberFromUser > 0) {
    //     numberOfPositives = numberOfPositives + 1;
    // } else {
    //     numberOfNegatives = numberOfNegatives + 1;
    // }

}

// For printing the number of positive numbers
System.out.println("Positive numbers: " + numberOfPositives);
// For printing the number of negative numbers
System.out.println("Negative numbers: " + numberOfNegative)s;

// For printing the percentage of positive numbers from all numbers

if (numberOfPositives + numberOfNegatives > 0) {
    // Print only if user has given numbers
    // to avoid dividing by zero
    double percentageOfPositives = 100.0 * numberOfPositives / (numberOfPositives + numberOfNegatives);
    System.out.println("Percentage of positive numbers: " + percentageOfPositives + "%");
}
```

![[Pasted image 20240907182148.png]]

![[Pasted image 20240907193318.png]]

![[Pasted image 20240907193342.png]]
