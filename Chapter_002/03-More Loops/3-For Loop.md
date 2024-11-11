Above, we learned how a `while` loop with a condition can be used to go through numbers in a certain interval.

The structure of this kind of loop is the following.

```java
int i = 0;
while (i < 10) {
    System.out.println(i);
    i++;
}
```

The above loop can be split into three parts. First we introduce the variable `i`, used to count the number of times the loop has been executed so far, and set its value to 0: `int i = 0;`. This is followed by the definition of the loop — the loop's condition is `i < 10` so the loop is executed as long as the value of the variable `i` is less than 10. The loop body contains the functionality to be executed `System.out.println(i);`, which is followed by increasing the value of the variable `i++`. The command `i++` is shorthand for `i = i + 1`.

The same can be achieved with a `for` loop like so.

```java
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}
```

A `for` loop contains four parts: (1) introducing the variable for counting the number of executions; (2) the condition of the loop; (3) increasing (or decreasing or changing) the value of the counter variable; and (4) the functionality to be executed.

```java
for (*introducing a variable*; *condition*; *increasing the counter*) {
    // Functionality to be executed
}
```

------------------------------------------------------------------------
```Java
public class Example {
    public static void main(String[] args) {
        for (int i = 0; i < 5; i++) {
           System.out.println(i);
        }   
    }
}
```

The example above prints the numbers from zero to four. The interval can also be defined using variables — the example below uses variables `start` and `end` to define the interval of numbers the loop goes through.

```java
int start = 3;
int end = 7;
for (int i = start; i < end; i++) {
    System.out.println(i);
}
```

We will continue practicing loops in the following exercises. You can use either a `while` loop with a condition, or a `for` loop.

![[Pasted image 20240907222748.png]]
![[Pasted image 20240907223010.png]]

**NOTE!**

### Exercises with multiple parts

Note, that from now on exercises can have multiple parts. All of the parts are counted as separate exercises, so for example the following exercise counts as two separate exercises. Exercises with multiple parts can also typically be submitted even if all parts are not ready — points for the completed parts are added to your points count. Submitting a partial solution does not prevent you from submitting the full solution later on.

![[Pasted image 20240907223314.png]]

**Continue...**

![[Pasted image 20240907223344.png]]
