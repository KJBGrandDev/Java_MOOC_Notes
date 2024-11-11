Let's now study an example where the method returns a value. The `main` method of the program calls a separate `start` method, inside of which two variables are created, the `sum` method is called, and the the value returned by the `sum` method is printed.

```java
public static void main(String[] args) {
    start();
}

public static void start() {
    int first = 5;
    int second = 6;

    int sum = sum(first, second);

    System.out.println("Sum: " + sum);
}

public static int sum(int number1, int number2) {
    return number1 + number2;
}
```

At the beginning of the `start` method's execution the call stack looks as in the following illustration since it was called from the `main` method. The method `main` has no variables of its own in this example:

```Java
start 
main
```

When the variables `first` and `second` have been created in the `start` method (i.e., the first two rows of that method have been executed), the situation is the following:

```Java
start 
	first = 5 
	second = 6 
main
```

The command `int sum = sum(first, second);` creates the variable `sum` in the method `start` and calls the method `sum`. The method `start` enters a waiting state. Since the parameters `number1` and `number2` are defined in the method `sum`, they are created right at the beginning of the method's execution, after which the values of the variables given as parameter are copied into them.

```Java
sum 
	number1 = 5 
	number2 = 6 
start 
	first = 5 
	second = 6 
sum // no value main
```

The execution of the method `sum` adds together the values of the variables `number1` and `number2`. The command `return` returns the sum of the numbers to the method that is one beneath it in the call stack - the method `start` in this case. The returned value is set as the value of the variable `sum`.

```Java
start 
	first = 5 
	second = 6 
	sum = 11 
main
```

After that, the print command is executed, and then we return to the `main` method. Once the execution reaches the end of the `main` method, the execution of the program ends.

## Method Calling Another Method

As we noticed earlier, other methods can be called from within methods. An additional example of this technique is given below. We'll create the method `multiplicationTable` that prints the multiplication table of the given number. The multiplication table prints the rows with the help of the `printMultiplicationTableRow` method.

```Java
public static void multiplicationTable(int max){
	int number = 1;
	while (number <= max){
		printMultiplicationTable(number,max);
		number++;
	}
}
public static void printMultiplicationTable(int number, int coefficient){
	int printable = number;
	while(printable <= number * coefficient){
		System.out.println(" " + printable);
		printable += number;
	}	
	System.out.println("");
}
```

The output of the method call `multiplicationTable(3)`, for instance, looks like this.

```Java
1 2 3 
2 4 6
3 6 9
```