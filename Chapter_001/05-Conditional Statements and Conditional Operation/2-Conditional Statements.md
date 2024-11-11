Our programs have so far been linear. In other words, the programs have executed from top to bottom without major surprises or conditional behavior. However, we usually want to add conditional logic to our programs. By this we mean functionality that's in one way or another dependent on the state of the program's variables.

To branch the execution of a program based on user input, for example, we need to use something known as a **conditional statement**. The simplest conditional statement looks something like this.

```Java
System.out.println("Hello, World!");

if(true){
	System.out.println("This code is unavoidable!");
}
// Hello World
// This code is unavoidable!
```

A conditional statement begins with the keyword `if` followed by parentheses. An expression is placed inside the parentheses, which is evaluated when the conditional statement is reached. The result of the evaluation is a boolean value. No evaluation occurred above. Instead, a boolean value was explicitly used in the conditional statement.

The parentheses are followed by a block, which is defined inside opening- `{` and closing `}` curly brackets. The source code inside the block is executed if the expression inside the parentheses evaluates to _true_.

```Java
if(expression / conditional statement){
// Source code executes if the conditional statement is "true"
}
```

Let's look at an example where we compare numbers in the conditional statement.

```Java
int number = 11;
if(number > 10){
	System.out.println("The number was greater than 10");
}
```

If the expression in the conditional statement evaluates to true, the execution of the program progresses to the block defined by the conditional statement. In the example above, the conditional is "if the number in the variable is greater than 10". On the other hand, if the expression evaluates to false, the execution moves on to the statement after the closing curly bracket of the current conditional statement.

**Note!** An `if` -statement is not followed by a semicolon since the statement doesn't end after the conditional.