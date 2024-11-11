Division of integers is a slightly trickier operation. The types of the variables that are part of the division determine the type of result achieved by executing the command. If all of the variables in the division expression are integers, the resulting value is an integer as well.

```Java
int result = 3 / 2;
System.out.println(result) // 1
```

The previous example prints 1: both 3 and 2 are integers, and the division of two integers always produces an integer.

```Java
int first = 3;
int second = 2;
double result = first / second;
System.out.println(result); // 1
```

The output 1 again, since first and second are (still) integers.

If the dividend or divisor (or both!) of the division is a floating point number, the result is a floating point number as well.

```Java
double whenDividendIsFloat = 3.0 / 2;
System.out.println(whenDividendIsFloat); // 1.5

double whenDivisorIsFloat = 3 / 2.0;
System.out.println(whenDivisorIsFloat); // 1.5
```

An integer can be converted into a floating point number by placing a type-casting operation `(double)` before it:
```Java
int first = 3;
int second = 2;

double result1 = (double) first / second;
System.out.println(result1) // 1.5

double result2 = first / (double) second;
System.out.println(result2) // 1.5

double result3 = (double) (first / second);
System.out.println(result3) // 1.0
```

The last example produces an incorrectly rounded result, because the integer division is executed before the type casting.

If the result of a division is assigned to an integer-type variable, the result is automatically an integer.

```Java
int integer = (int) 3.0 / 2;
System.out.println(integer) // 1
```

The next example prints "1.5"; the dividend is converted into a floating-point number by multiplying it with a floating-point number prior to executing the division.

```Java
int dividend = 3;
int divisor = 2;

double result = 1.0 * dividend / divisor;
System.out.println(result); // 1.5
```