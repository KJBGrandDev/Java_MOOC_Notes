The definition of a method tells whether that method returns a value or not. If it does, the method definition has to include the type of the returned value. Otherwise the keyword `void` is used in the definition. The methods we've created so far have been defined with the keyword `void`, meaning that they have not returned values.

```java
public static **void** incrementByThree() {
    ...
}
```

The keyword `void` means that the method returns nothing. If we want the method to return a value, the keyword must be replaced with the type of the return variable. In the following example, there is a method called `alwaysReturnsTen` which returns an integer-type (`int`) variable (in this case the value 10).

To actually return a value, we use the command `return` followed by the value to be returned (or the name of the variable whose value is to be returned).

```java
public static int alwaysReturnsTen() {
    return 10;
}
```

The method defined above returns an `int`-type value of `10` when called. For the return value to be used, it must be stored in a variable. This is done the same way as regular value assignment to a variable, by using an equals sign.

```java
public static void main(String[] args) {
    int number = alwaysReturnsTen();

    System.out.println("the method returned the number " + number);
}
```

The return value of the method is placed in an `int` type variable as with any other `int` value. The return value can also be used in any other expression.

```java
double number = 4 * alwaysReturnsTen() + (alwaysReturnsTen() / 2) - 8;

System.out.println("the result of the calculation " + number);
```

All the variable types we've encountered so far can be returned from a method.

![[Pasted image 20240912000704.png]]

When execution inside a method reaches the command `return`, the execution of that method ends and the value is returned to the calling method.

The lines of source code following the command `return` are never executed. If a programmer adds source code after the return to a place which can never be reached during the method's execution, the IDE will produce an error message.

For the IDE, a method such as the following is faulty.

```java
public static int faultyMethod() {
    return 10;
    System.out.println("I claim to return an integer, but I don't.");
}
```

The next method works since it is possible to reach every statement in it — even though there is source code below the return command.

```Java
public static int functioningMethod(int parameter){
	if(parameter > 10){
		return 10;
	}
	System.out.println("The number received as parameter is ten or less.");

	return parameter;
}
```

If a method has the form `public static void nameOfMethod()` it is possible to return from it — in other words, to stop its execution in that place — with the `return` command that is not followed by a value. For instance:

```java
public static void division(int numerator, int denominator) {
    if (denominator == 0) {
        System.out.println("Can not divide by 0!");
        return;
    }

    System.out.println("" + numerator + " / " + denominator + " = " + (1.0 * numerator / denominator));
}
```