If the expression inside the parentheses of the conditional statement evaluates to false, then the execution of the code moves to the statement following the closing curly bracket of the current conditional statement. This is not always desired, and usually we want to create an alternative option for when the conditional expression evaluates to false.

This can be done with the help of the `else` command, which is used together with the `if` command.

```Java
int number = 4;

if(number > 5){
	System.out.println("Your number is greater than five!");
} else {
	System.out.println("Your number is five or less!");
}
// Your number is five or less!
```

If an `else` branch has been specified for a conditional statement, the block defined by the else branch is run in the case that the condition of the conditional statement is false. The `else`-command is placed on the same line as the closing bracket of the block defined by the `if`-command.