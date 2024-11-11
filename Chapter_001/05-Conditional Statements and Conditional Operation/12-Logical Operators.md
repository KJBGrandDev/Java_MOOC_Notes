The expression of a conditional statement may consist of multiple parts, in which the logical operators **and** `&&`, **or** `||`, and **not** `!` are used.

- An expression consisting of two expressions combined using the and-operator is true, if and only if both of the combined expressions evaluate to true.

- An expression consisting of two expressions combined using the or-operator is true if either one, or both, of the combined expressions evaluate to true.

- Logical operators are not used for changing the boolean value from true to false, or false to true.

In the next example we combine two individual conditions using `&&`, i.e., the and-operator. The code is used to check if the number in the variable is greater than or equal to 5 and less than or equal to 10. In other words, whether it's within the range of 5-10:

```Java
System.out.println("Is the number within the range 5-10: ");
int number = 7;

if(number >= 5 && number <= 10){
	System.out.println("It is! :)");
} else {
	System.out.println("It is not :(");
}
// Is the number within the range 5-10:
// It is! :)
```

In the next one we provide two conditions using `||`, i.e., the or-operator: is the number less than zero or greater than 100. The condition is fulfilled if the number fulfills either one of the two conditions:

```Java
System.out.println("Is the number less than 0 or greater than 100");
int number = 145;

if(number < 0 || number > 100){
	System.out.println("It is! :)");
} else {
	System.out.println("It is not :(");
}
// Is the number less than 0 or greater than 100
// It is! :)
```

In this example we flip the result of the expression `number > 4` using `!`, i.e., the not-operator. The not-operator is written in such a way that the expression to be flipped is wrapped in parentheses, and the not-operator is placed before the parentheses.

```Java
int number = 7;

if(!(number > 4)){
	System.out.println("The number is not greater than 4.");
} else {
	System.out.println("The number is greater than 4.");
}
// The nubmer is greater than 4
```

Below is a table showing the operation of expressions containing logical operators.

![[Pasted image 20240901192132.png]]
