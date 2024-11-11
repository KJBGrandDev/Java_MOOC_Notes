Comments have many purposes, and one of them is explaining how the code works to oneself when searching for bugs. The execution of a relatively simple program is described below through the use of comments.

```java
/*
 Prints the numbers from ten to one.
Each number is printed on its own line.
*/

// We create an integer variable named value,
// assigning the value 10 to it.
int value = 10;

// The loop execution continues until
// the value of the variable named value is less than or equal to
// zero. The excution doesn't stop _immediately_ when the value zero
// is assigned to the variable, but only when the condition of the
// loop is evaluated the following time.
// This always happens after the loop has executed
while (value > 0) {
    // we print out the value in the variable and a new line
    System.out.println(value);
    // we decrement the value by one
    value = value - 1;
}
```

Comments have no impact on the execution of the program, i.e., the program works in the same way with the comments as it does without them.

The comment style displayed above that is intended for learning purposes is, however, too elaborate for real development, where the goal is for the source code to be **self documenting**. This means that the functionality of the program should be evident from the way classes, methods, and variables are named.

The example can be "commented out" by encapsulating the code into an appropriately named method. Below are two examples of methods that do this - one of the methods is more general in its purpose compared to the other. The more general method assumes, however, that the user knows which of the two parameters is assigned the higher value and which the lower.

```java
public static void printValuesFromTenToOne() {
    int value = 10;
    while (value > 0) {
        System.out.println(value);
        value = value - 1;
    }
}
```

```java
public static void printValuesFromLargestToSmallest(int start, int end) {
    while (start >= end) {
        System.out.println(start);
        start = start - 1;
    }
}
```