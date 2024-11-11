A loop does not stop executing immediately when its condition evaluates to true. A loop's condition is evaluated at the start of a loop, meaning when (1) the loop starts for the first time or (2) the execution of a previous iteration of the loop body has just finished.

Let's look at the following loop.

```java
int number = 1;

while (number != 2) {
    System.out.println(number);
    number = 2;
    System.out.println(number);
    number = 1;
}
```

It prints the following:

```Java
1 2 1 2 1 2 ...
```

Even though `number` equals 2 at one point, the loop runs forever.

**The condition of a loop is evaluated when the execution of a loop starts and when the execution of the loop body has reached the closing curly bracket.** If the condition evaluates to `true`, execution continues from the top of the loop body. If the condition evaluates to `false`, execution continues from the first statement following the loop.

This also applies to `for` loops. In the example below, it would be incorrect to assume that the loop execution ends when `i` equals 100. However, it doesn't.

```java
for (int i = 0; i != 100; i++) {
    System.out.println(i);
    i = 100;
    System.out.println(i);
    i = 0;
}
```

The loop above never stops executing.

