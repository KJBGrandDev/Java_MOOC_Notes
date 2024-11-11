**Parameters** are values given to a method that can be used in its execution. The parameters of a method are defined on the uppermost line of the method within the parentheses following its name. The values of the parameters that the method can use are copied from the values given to the method when it is executed.

In the following example a parameterized method `greet` is defined. It has an `int` type parameter called `numOfTimes`.

```java
public static void greet(int numOfTimes) {
    int i = 0;
    while (i < numOfTimes) {
        System.out.println("Greetings!");
        i++;
    }
}
```

We will call the method `greet` with different values. The parameter `numOfTimes` is assigned the value `1`on the first call, and `3`on the second.

```java
public static void main(String[] args) {
    greet(1);
    System.out.println("");
    greet(3);
}
```

```Java
Greetings!

Greetings! 
Greetings! 
Greetings!
```

Just like when calling the predefined method `System.out.println`, you can pass an expression as a parameter.

```java
public static void main(String[] args) {
    greet(1 + 2);
}
```

```Java
Greetings! 
Greetings! 
Greetings!
```

If an expression is used as a parameter for a method, the expression is evaluated prior to the method call. Above, the expression evaluates to `3` and the final method call is of the form `greet(3);`.

![[Pasted image 20240908234224.png]]

![[Pasted image 20240908235745.png]]
