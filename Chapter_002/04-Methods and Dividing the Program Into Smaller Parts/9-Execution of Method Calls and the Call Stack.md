How does the computer remember where to return after the execution of a method?

The environment that executes Java source code keeps track of the method being executed in the call stack. **The call stack** contains frames, each of which includes information about a specific method's internal variables and their values. When a method is called, a new frame containing its variables is created in the call stack. When the execution of a method ends, the frame relating to a method is removed from the call stack, which leads to execution resuming at the previous method of the stack.

The right side of the visualization below displays the functioning of the call stack. When a method is called, a new frame is created in the stack, which is removed upon exit from the method call.

--------------------------------------------------------------------


When a method is called, the execution of the calling method is left waiting for the execution of the called method to end. This can be visualized with the help of a call stack. The call stack refers to the stack formed by the method calls — the method currently being executed is always on the top of the stack, and when that method has finished executing the execution moves on to the method that is next on the stack. Let's examine the following program:
```Java
public static void main(String[] args){
	System.out.println("Hello World");
	printNumber();
	System.out.println("Bye bye world!");
}
public static void printNumber(){
	System.out.println("Number");
}
```

The execution begins from the first line of the `main` method when the program is run. The command on this line prints the text `"Hello world!"`. The call stack of the program looks as follows:
```Java
main
```

Once the print command has been executed, we move on to the next command, which calls the method `printNumber`. Calling this method moves the execution of the program to the beginning of the method `printNumber`. Meanwhile, the `main` method will await for the execution of the method `printNumber` to end. While inside the method `printNumber`, the call stack looks like this:

```Java
printNumber
main
```

Once the method `printNumber` completes, we return to the method that is immediately below the method `printNumber` in the call stack — which in this case is the method `main`. `printNumber` is removed from the call stack, and the execution continues from the line after the `printNumber` method call in the `main` method. The state of the call stack is now the following:

```Java
main
```