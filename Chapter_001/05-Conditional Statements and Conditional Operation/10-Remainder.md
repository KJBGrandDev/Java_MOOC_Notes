The modulo operator is a slightly less-used operator, which is, however, very handy when we want to check the divisibility of a number, for example. The symbol for the modulo operator is `%`.

```java
int remainder = 7 % 2;
System.out.println(remainder); // prints 1
System.out.println(5 % 3); // prints 2
System.out.println(7 % 4); // prints 3
System.out.println(8 % 4); // prints 0
System.out.println(1 % 2); // prints 1
```

If we want to know whether the number given by the user is divisible by four hundred, we check if the remainder is zero after taking the modulo of the number and four hundred.

```Java
Scanner reader = new Scanner(System.in);

int number = Integer.valueOf(reader.nextLine());
int remainder = number % 400;

if(remainder == 0){
	System.out.println("The number " + number + " is divisible by four hundred.");
} else {
	System.out.println("The number " + number + " is not divisible by four hundred.");
}
```

Since the modulo is an operation just like other calculations, it can be a part of an expression in a conditional statement.

```Java
Scanner reader = new Scanner(System.in);

int number = Integer.valueOf(reader.nextLine());

if (number % 400 == 0) {
    System.out.println("The number " + number + " is divisible by four hundred.");
} else {
    System.out.println("The number " + number + " is not divisible by four hundred.");
}
```