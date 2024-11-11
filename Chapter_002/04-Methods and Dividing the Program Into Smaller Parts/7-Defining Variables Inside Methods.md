Defining variables inside methods is done in the same manner as in the "main program". The following method calculates the average of the numbers it receives as parameters. Variables `sum` and `avg` are used to help in the calculation.

```Java
public static double average(int number1, int number2, int number3){
	int sum = number1 + number2 + number3;
	double avg = sum / 3.0;
}
```

One way to call the method is as follows.

```Java
public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Enter the first number: ");
	int first = Integer.valueOf(scanner.nextLine());

	System.out.println("Enter the second number: ");
	int second = Integer.valueOf(scanner.nextLine());

	System.out.println("Enter the third number: ");
	int third = Integer.valueOf(scanner.nextLine());

	double averageResult = average(first,second,third);

	System.out.println("The average of the numbers: " + averageResult);
}
```

Variables defined in a method are only visible inside that method. In the example above, this means that the variables `sum` and `avg` defined inside the method `average` are not visible in the main program. A typical mistake while learning programming is to try and use a method in the following way.

```java
public static void main(String[] args) {
    int first = 3;
    int second = 8;
    int third = 4;

    average(first, second, third);

    // trying to use a method's internal variable, DOES NOT WORK!
    System.out.print("The average of the numbers: " + avg);
}
```

In the above example, an attempt is made to use the variable `avg` that has been defined inside the method `average` and print its value. However, the variable `avg` only exists inside the method `average`, and it cannot be accessed outside of it.

The following mistakes are also commonplace.

```java
public static void main(String[] args) {
    int first = 3;
    int second = 8;
    int third = 4;

    // trying to use the method name only, DOES NOT WORK!
    System.out.print("The average of the numbers: " + average);
}
```

Above, there is an attempt to use the name of the method `average` as if it were a variable. However, a method has to be called.

As well as placing the method result into a helper variable, another way that works is to execute the method call directly inside the print statement:

```java
public static void main(String[] args) {
    int first = 3;
    int second = 8;
    int third = 4;

    // calling the method inside the print statement, DOES WORK!
    System.out.print("The average of the numbers: " + average(first, second, third));
}
```

Here, the method call occurs first returning the value **5.0**, which is then printed with the help of the print statement.