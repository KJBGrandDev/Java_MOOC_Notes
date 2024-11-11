So far we have been using a loop with the boolean `true` in its parenthesis, meaning the loop continues forever (or until the loop is ended with the `break` command ).

Actually, the parenthesis of a loop can contain a conditional expression, or a condition, just like the parenthesis of an `if` statement. The `true` value can be replaced with an expression, which is evaluated as the program is executed. The expression is defined the same way as the condition of a conditional statement.

The following code prints the numbers 1,2,...,5. When the value of the variable `number` is more than 5, the `while`-condition evaluates to false and the execution of the loop ends for good.

```java
int number = 1;

while (number < 6) {
    System.out.println(number);
    number++;
}
```

The code above can be read "As long as the value of the variable number is less than 6, print the value of the variable number and increase the value of the variable number by one".

Above, the value of the variable `number` is increased by one every time the loop body is executed.