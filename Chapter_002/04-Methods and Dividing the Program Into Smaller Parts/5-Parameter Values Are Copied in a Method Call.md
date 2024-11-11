As a method is called **the values of its parameters are copied**. In practice, this means that both the main method and the method to be called can use variables with the same name. However, changing the value of the variables inside the method does not affect the value of the variable in the main method that has the same name. Let's examine this behavior with the following program.

```java
public class Example {
    public static void main(String[] args) {
        int min = 5;
        int max = 10;

        printNumbers(min, max);
        System.out.println();

        min = 8;

        printNumbers(min, max);
    }

    public static void printNumbers(int min, int max) {
        while (min < max) {
            System.out.println(min);
            min++;
        }
    }
}
```

The output of the program is:

```Java
5 6 7 8 9

8 9
```

Beneath, you'll find the same program visualized step-by-step. Changing the values of the variables in the method printNumbers does not affect the values in the main method, even though they have the same names.

```Java
Cant copy the process
```

So, method parameters are distinct from the variables (or parameters) of other methods, even if they had the same name. As a variable is passed to a method during a method call, the value of that variable gets copied to be used as the value of the parameter variable declared in the method definition. Variables in two separate methods are independent of one another.

To further demonstrate this point, let's consider the following example. We define a variable called `number` in the main method. That variable is passed as a parameter to the method `incrementByThree`.

```java
// main program
public static void main(String[] args) {
    int number = 1;
    System.out.println("The value of the variable 'number' in the main program: " + number);
    incrementByThree(number);
    System.out.println("The value of the variable 'number' in the main program: " + number);
}

// method
public static void incrementByThree(int number) {
    System.out.println("The value of the method parameter 'number': " + number);
    number = number + 3;
    System.out.println("The value of the method parameter 'number': " + number);
}
```

The execution of the program produces the following output.

```Java
The value of the variable 'number' in the main program: 1 
The value of the method parameter 'number': 1 
The value of the method parameter 'number': 4 
The value of the variable 'number' in the main program: 1
```

When the variable `number` is incremented inside the method, there's no issue. This, however, is not reflected in the `number` variable of the main program. The `number` variable living in the main program is different from the `number` variable of the method.

The parameter `number` is copied for the method's use, i.e., a new variable called `number` is created for `incrementByThree` method, to which the value of the variable `number` in the main program is copied during the method call. The variable `number` inside the method `incrementByThree` exists only for the duration of the method's execution and has no relation to the variable of the same name in the main program.

![[Pasted image 20240911235655.png]]

```Java
// Answer
10
```

