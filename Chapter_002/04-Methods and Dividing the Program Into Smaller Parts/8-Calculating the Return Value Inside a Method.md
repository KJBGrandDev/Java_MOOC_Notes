The return value does not need to be entirely pre-defined - it can also be calculated. The return command that returns a value from the method can also be given an expression that is evaluated before the value is returned.

In the following example, we'll define a method sum that adds the values of two variables and returns their sum. The values of the variables to be summed are received as method parameters.

```Java
public static int sum(int first, int second){
	return first + second;
}
```

When the execution of the method reaches the statement `return first + second;`, the expression `first + second` is evaluated, and then its value is returned.

The method is called in the following way. Below, the method is used to add the numbers 2 and 7 together. The value resulting from the method call is placed into the variable `sumOfNumbers`.

```Java
int sumOfNumbers = sum(2,7);
// sumOfNumbers is now 9
```

Let's expand the previous example so that the numbers are entered by a user.

```Java
public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Enter the first number: ");
	int first = Integer.valueOf(scanner.nextLine());

	System.out.println("Enter the second number: ");
	int second = Integer.valueOf(scanner.nextLine());

	System.out.println("The combined sum of the numbers is : " + sum(first,second));
}

public static int sum(int first, int second){
	return first + second;
}
```

In the example above, the method's return value is not stored in a variable but is instead directly used as part of the print operation. The print command's execution is done by the computer first evaluating the string `"The combined sum of the numbers is: "+ sum(first, second)`. The computer first looks for the variables `first` and `second` and copies their values as the values ​​of the method `sum`'s parameters. The method then adds the values of the parameters ​​together, after which it returns a value. This value takes the place of the `sum` method call, whereby the sum is appended to the string `"The combined sum of the numbers is: "`.

Since the values passed to a method are copied to its parameters, the names of the parameters and the names of the variables defined on the side of the caller have, in fact, nothing to do with each other. In the previous example, both the variables of the main program and the method parameters were named the same (`first` and `second`) "by accident". The code below will function in precisely the same manner even though the variables are named differently:

```Java
public static void main(String[] args){
	Scanner scanner = new Scanner(System.in);

	System.out.println("Enter the first number: ");
	int number1 = Integer.valueOf(scanner.nextLine());

	System.out.println("Enter the second number: ");
	int number2 = Integer.valueOf(scanner.nextLine());

	System.out.println("The total sum of the numbers is: " +sum(number1,number2));
}
public static int sum(int first, int second){
	return first + second;
}
```

Now the value of the variable `number1` is copied as the value of the method parameter `first`, and the value of the variable `number2` is copied as the value of the parameter `second`.