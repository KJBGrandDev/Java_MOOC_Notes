# Changing a Value Assigned to a Variable

A variable exists from the moment of its declaration, and its initial value is preserved until another value is assigned to it.

You can change a variable's value using a statement that comprises the variable name, an equal sign, and the new value to be assigned.

Remember to keep in mind that the variable type is only stated during the initial value declaration.
```Java
int number = 123;
System.out.println("The value of the variable is: " + number);

number = 42;

```

Let's look at the preceding program's execution step by step. When a variable appears in the program for the first time, i.e., the computer is told both its type(in this case "int") and its name(in this case "number"), the computer creates a "named container" for the variable. Then, the value on the right side of the equals sign is copied into this named container.
![[Pasted image 20240827232103.png]]
Whenever a variable is referenced by its "name" in a program - here, we want to print the string "The value of the variable is " followed by the value of the "number" variable - its value is retrieved from a container that has the corresponding name.
![[Pasted image 20240827232310.png]]
Whenever a value is assigned to a variable(here number = 42), a check is run to see whether a container with the given name already exists. If one does, a new value is copied in the place of the old value, and the old value disappears. If a container of the variable name is not found, the program execution ends in an "error message", or it fails to run.
![[Pasted image 20240827232513.png]]
The variable is then referenced again by its name in the program - we again want to print the string "The value of the variable is " followed by the value of the "number" variable. We proceed as normal, retrieving the value of "number" from a container having its name.
![[Pasted image 20240827232710.png]]
At the end of the program, you'll notice that the original value of the variable has vanished. A variable can hold "only" one value at a time.