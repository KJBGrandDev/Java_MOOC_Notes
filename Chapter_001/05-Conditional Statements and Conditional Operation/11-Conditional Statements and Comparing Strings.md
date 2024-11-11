Even though we can compare integers, floating point numbers, and boolean values using two equals signs (`variable1 == variable2`), we cannot compare the equality of strings using two equals signs.

You can try this with the following program:

```Java
Scanner reader = new Scanner(System.in);

System.out.println("Enter the first string");
String first = reader.nextLine();
System.out.println("Enter the second string");
String second = reader.nextLine();

if(first == second){
	System.out.println("The strings were the same!");
} else {
	System.out.prinlt("The strings were different!");
}
```

```Java
Enter the first string 
**same**
Enter the second string 
**same** 
The strings were different!

Enter the first string 
**same** 
Enter the second string 
**different** 
The strings were different!
```

This has to do with the internal workings of strings as well as how variable comparison is implemented in Java. 

In practice, the comparison is affected by how much information a variable can hold — strings can hold a limitless amount of characters, whereas integers, floating-point numbers, and boolean values always contain a single number or value only. 

Variables that always contain only one number or value can be compared using an equals sign, whereas this doesn't work for variables containing more information. We will return to this topic later in this course.

When comparing strings we use the `equals`-command, which is related to string variables. The command works in the following way:

```Java
Scanner reader = new Scanner(System.in);

System.out.println("Enter a string");
String input = reader.nextLine();

if(input.equals("a string")){
	System.out.println("Great! You read the instructions correctly.);
} else {
	System.out.println("Missed the mark!");
}
```

```Java
Enter a string 
**ok!**
Missed the mark!

Enter a string
**a string**
Great! You read the instructions correctly.
```

The equals command is written after a string by attaching it to the string to be compared with a dot. 

The command is given a parameter, which is the string that the variable will be compared against. If the string variable is being directly compared with a string, then the string can be placed inside the parentheses of the equals-command within quotation marks. 

Otherwise, the name of the string variable that holds the string to be compared is placed inside the parentheses.

In the example below the user is prompted for two strings. We first check to see if the provided strings are the same, after which we'll check if the value of either one of the two strings is "two strings".

```java
Scanner reader = new Scanner(System.in);

System.out.println("Input two strings");
String first = reader.nextLine();
String second = reader.nextLine();

if (first.equals(second)) {
    System.out.println("The strings were the same!");
} else {
    System.out.println("The strings were different!");
}

if (first.equals("two strings")) {
    System.out.println("Clever!");
}

if (second.equals("two strings")) {
    System.out.println("Sneaky!");
}
```

```Java
Input two strings 
**hello** 
**world** 
The strings were different!

Input two strings 
**two strings** 
**world** 
The strings were different! 
Clever!

Input two strings 
**same** 
**same** 
The strings were the same!
```