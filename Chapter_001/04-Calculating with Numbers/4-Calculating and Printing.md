The command `System.out.println` prints the value of a variable. The string literal to be printed, which is marked by quotation marks, can be appended with other content by using the operation `+`.
```Java
int length = 42;
System.out.println("Length" + length); //Length 42
```

```Java
System.out.println("here is an integer --> " + 2);
System.out.println(2 + " <-- here is an integer");
// here is an integer —> 2 
// 2 <— here is an integer
```

If one of the operands of the operation `+` is a string, the other operand will be changed into a string too during program execution. In the example below, the integer `2` is turned into the string "2", and a string has been appended to it.

The precedence introduced earlier also apply here:
```Java
System.out.println("Four: " + (2 + 2)); // Four: 4
System.out.println("But! Twenty-two: " + 2 + 2); // But! Twenty-two: 22 
```

Applying this knowledge, we can create an expression consisting of some text and a variable, which is evaluated in connection with the printing:
```Java
int x = 10;

System.out.println("The value of the variable x is: " + x);
// The value of the variable x is: 10
int y = 5;
int z = 6;

System.out.println("y is " + y + " and z is " + z);
// y is 5 and z is 6
```

**NOTE: From me**
- This process is similar to Javascript's method called "Coercion"
- Type Coercion refers to **the process of automatic or implicit conversion of values from one data type to another**. This includes conversion from Number to String, String to Number, Boolean to Number, etc.