One common subproblem type is to "do something a certain amount of times". What's common to all these programs is repetition. Some functionality is done repeatedly, and a counter variable is used to keep track of the repetitions.

The following program calculates the product 4 * 3 somewhat clumsily, i.e., as the sum 3 + 3 + 3 + 3:

```java
int result = 0;

int i = 0;
while (true) {
    result += 3; // shorthand for result = result + 3
    i++;  // shorthand for i = i + 1

    if (i == 4) {
        break;
    }
}

System.out.println(result);
```

The same functionality can be achieved with the following code.

```java
int result = 0;

int i = 0;
while (i < 4) {
    result += 3; // shorthand for result = result + 3
    i++;  // shorthand for i = i + 1

}

System.out.println(result);
```

Or by using a for loop as seen in the following.

```java
int result = 0;

for (int i = 0; i < 4; i++) {
    result += 3;
}

System.out.println(result);
```

