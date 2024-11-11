When a computer executes program code, it does it one command at a time, always advancing exactly as specified by the code. When a value is assigned to a variable, the same chain of events always occurs: the value on the right-hand side of the equality sign is copied and assigned to the variable on the left-hand side (i.e., copied to the location specified by that variable).

It's crucial for a programmer to understand that assigning a value to a variable always does the same thing.

Here's three common misunderstandings related to assigning a value to a variable:

- Viewing value assignment as a transfer instead of a copy operation: once `first = second` has been executed, it's often assumed that the value of the variable `second` has been moved to the value of the variable `first`, and that the variable `second` no longer holds a value, or that its value is 0, for instance. This is incorrect, as executing `first = second` means that the value in the position specified by `second` is merely copied to the place specified by the variable `first`. Hence, the variable `second` is not modified.

- Viewing value assignment as creating a dependency instead of being a copy operation: once `first = second` has been executed, it's often assumed that any change in the value of the variable `second` is automatically also reflected in the value of the variable `first`. This is incorrect; assignment — i.e., copying — is a one-off event. It only occurs when the program code `first = second` is executed.

- The third misunderstanding concerns the direction of copying: it's often thought that in executing `first = second` the value of the variable `second` is set as the value of the variable `first`. The confusion also manifests itself in situations where the programmer accidentally writes e.g. `42 = value` — fortunately, IDEs provide support on this issue too.

Perhaps the best way to understand a program's execution flow is through the use of pen and paper. As you're reading the program, write down the names of any new variables, while making a note of how the values of the variables in the code change line by line. Let's demonstrate the execution with the following program code:

```java
line 1: int first = (1 + 1);
line 2: int second = first + 3 * (2 + 5);
line 3:
line 4: first = 5;
line 5:
line 6: int third = first + second;
line 7: System.out.println(first);
line 8: System.out.println(second);
line 9: System.out.println(third);
```

The execution flow of the program above has been broken down below.

```Java
line 1: initiate a variable first 
line 1: copy the result of the calculation 1 + 1 as the value of the variable first 
line 1: the value of the variable first is 2 
line 2: create the variable second 
line 2: calculate 2 + 5, 2 + 5 -> 7 
line 2: calculate 3 * 7, 3 * 7 -> 21 
line 2: calculate first + 21 
line 2: copy the value of the variable first into the calculation, its value is 2 
line 2: calculate 2 + 21, 2 + 21 -> 23 
line 2: copy 23 to the value of the variable second 
line 2: the value of the variable second is 23 
line 3: (empty, do nothing) 
line 4: copy 5 to the value of the variable first 
line 4: the value of the variable first is 5 
line 5: (empty, do nothing) 
line 6: create variable third 
line 6: calculate first + second 
line 6: copy the value of the variable first into the calculation, its value is 5 
line 6: calculate 5 + second 
line 6: copy the value of the variable second into the calculation, its value is 23 
line 6: calculate 5 + 23 -> 28 
line 6: copy 28 to the value of the variable third 
line 6: the value of the variable third is 28 
line 7: print the variable first 
line 7: copy the value of the variable first for the print operation, its value is 5 
line 7: print the value 5 
line 8: print the variable second 
line 8: copy the value of the variable second for the print operation, its value is 23 
line 8: print the value 23 
line 9: print the variable third 
line 9: copy the value of the variable third for the print operation, its value is 28 
line 9: we print the value 28
```