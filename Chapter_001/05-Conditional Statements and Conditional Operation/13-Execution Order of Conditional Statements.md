Let's familiarize ourselves with the execution order of conditional statements through a classic programming exercise.

_'Write a program that prompts the user for a number between one and one hundred, and prints that number. If the number is divisible by three, then print "Fizz" instead of the number. If the number is divisible by five, then print "Buzz" instead of the number. If the number is divisible by both three and five, then print "FizzBuzz" instead of the number.'_

The programmer begins solving the exercise by reading the exercise description and by writing code according to the description. The conditions for execution are presented in a given order by the description, and the initial structure for the program is formed based on that order. The structure is formed based on the following steps:

- Write a program that prompts the user for a number and prints that number.

- If the number is divisible by three, then print "Fizz" instead of the number.

- If the number is divisible by five, then print "Buzz" instead of the number.

- If the number is divisible by both three and five, then print "FizzBuzz" instead of the number.

If-type conditions are easy to implement using `if - else if - else` -conditional statements. The code below was written based on the steps above, but it does not work correctly, which we can see from the example.

```Java
Scanner reader = new Scanner(System.in);
int number = Integer.valueOf(scanner.nextLine());

if (number % 3 == 0){
	System.out.println("Fizz");
} else if (number % 5 == 0){
	System.out.println("Buzz");
} else if (number % 3 == 0 && number % 5 == 0){
	System.out.println("FizzBuzz");
} else {
	System.out.println(number);
}
// 3 Fizz
// 4 4
// 5 Buzz
// 15 Fizz
```

The problem with the previous approach is that **the parsing of conditional statements stops at the first condition that is true**. E.g., with the value 15 the string "Fizz" is printed, since the number is divisible by three (15 % 3 == 0).

One approach for developing this train of thought would be to first find the **most demanding condition**, and implement it. After that, we would implement the other conditions. In the example above, the condition "if the number is divisible by both three **and** five" requires two things to happen. Now the train of thought would be:

1. Write a program that reads input from the user.

2. If the number is divisible by both three and five, then print "FizzBuzz" instead of the number.

3. If the number is divisible by three, then print "Fizz" instead of the number.

4. If the number is divisible by five, then print "Buzz" instead of the number.

5. Otherwise the program prints the number given by the user.

Now the problem seems to get solved.

```Java
Scanner reader = new Scanner(System.in);

int number = Integer.valueOf(reader.nextLine());

if (number % 3 == 0 && number % 5 == 0){
	System.out.println("FizzBuzz");
} else if (number % 3 == 0){
	System.out.println("Fizz");
} else if (number % 5 == 0){
	System.out.println("Buzz");
} else {
	System.out.println(number);
}

// 2 2
// 5 Buzz
// 30 FizzBuzz
```