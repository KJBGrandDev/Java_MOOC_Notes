"String" is shorthand for the term "String of characters". It describes how the computer sees text on a fundamental level: "as a sequence of individual characters".

In practice:
- Variables are "named containers" that contain information of some specified type and have a name.
- A "String" variable is declared in a program by stating the "type" of the variable (String) and its name (myString, for instance).
- Typically a variable is also assigned a value during its declaration (Java Initialization?)

A string variable called "message" that is assigned the value "Hello World!" is declared like this:
```Java
String message = "Hello World!";
```

When a variable is created, a specific container is made available within the program. The content of which can later be referenced (Same with Javascript's Non-Primitive Objects, object referencing)

For instance, creating and printing a "string variable" is done as shown below:
```Java
String message = "Hello World!";

System.out.println(message);// String variable, message is referenced
```

A string enclosed in a programming language's quotation marks is called a "String literal", i.e., "a string with a specified value".

A common programming "mistake" is trying to put a quotation marks around variable names.

If there were quotation marks around the string variable "message", the program would print the text "message" instead of the "Hello World!" text held by the string variable "message".
```Java
String message = "Hello World!";

System.out.println("message"); //prints message
System.out.println(message); //prints Hello World!
```