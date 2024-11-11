An _expression_ is a **combination of values** that is **turned into another value** through a calculation or evaluation.

The _statement_ below includes the expression `1 + 1 + 3 * 2 + 5`, which is evaluated prior to its assignment to the variable.

```Java
int calculationWithoutParentheses = 1 + 1 + 3 * 2 + 5;
```

The **evaluation of an expression** is **always performed** before **its value is assigned to a variable**. As such, the calculation "1 + 1 + 3 * 2 + 5" in the example above is performed before the result is assigned to the variable.

An expression is evaluated where it occurs in the program's source code. As such, the evaluation can occur within a print statement, if the expression is used in calculating the value of the print statement's parameter.
```Java
int first = 2;
int second = 4;

System.out.println(first + second); //prints 6
System.out.println(2 + second - first - second); //prints 0
```

An expression does not change the value stored in a variable unless the expression's result is assigned to a variable or used as a parameter, for instance, in printing.
```Java
int first = 2;
int second = 4;

//the expression below does not work, since
//the result is not assigned to any variable
//or given as a parameter to a print statement
first + second;
```