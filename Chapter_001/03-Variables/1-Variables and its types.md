A variable can be thought of as a container in which information of a given "type" can be stored. 

Examples of these different types include text(String), whole numbers(int), floating-point numbers(double), and whether something is true or false(boolean). A value is a assigned to a variable using the equals sign.
```Java
int months = 12;
```

In the statement above, the value of 12 is assigned on an "integer" variable called "months". The statement above could be read as: "The variable months is assigned the value 12".

A variable's value can be joined to a string using the " + " operator, as seen on the following examples:
```Java
String text = "contains text";
int wholeNumber = 123;
double floatingPoint = 3.141592653;
boolean trueOrFalse = true;

System.out.println("Text variable: " + text);
System.out.println("Integer variable: " + wholeNumber);
System.out.println("Floating point variable: " + floatingPoint);
System.out.println("Boolean: " + trueOrFalse);
```
```Java
//Output
Text variable: contains text
Integer variable: 123
Floating point variable: 3.141592653
Boolean: true
```
