A method can be defined with multiple parameters. When calling such a method, the parameters are passed in the same order.

```Java
public static void sum(int first, int second){
	System.out.println("The sum of the numbers " + first + " and " + second + " is " + (first + second));
}
```

```Java
sum(3, 5);

int number1 = 2;
int number2 = 4;

sum(number1, number2);
```

```Java
The sum of numbers 3 and 5 is 8 
The sum of numbers 2 and 4 is 6
```

![[Pasted image 20240910222051.png]]
![[Pasted image 20240910222736.png]]
