### Learning Objectives

- You are familiar with the concepts of a method parameter, a method's return value, and a program's call stack.

- You know how to create methods and how to call them from both the main program (the `main` method) as well as from inside other methods.

- You can create parameterized and non-parameterized methods, and you can create methods that return a value.

So far, we've used various commands: value assignment, calculations, conditional statements, and loops.

Printing to the screen has been done with the statement `System.out.println()`, and the reading of values with `Integer.valueOf(scanner.nextLine())`. `if` has been used in conditional statements, and `while` and `for` in loops. We notice that printing and reading operations somewhat differ from `if`, `while`, and `for` in that the print and read commands are followed by parentheses, which may include parameters passed to the command. The ones that "end in parentheses" are not actually commands, but methods.

Technically speaking, **a method** is a named set of statements.

It's a piece of a program that can be called from elsewhere in the code by the name given to the method. For instance `System.out.println("I am a parameter given to the method!")` calls a methods that performs printing to the screen. The internal implementation of the method — meaning the set of statements to be executed — is hidden, and the programmer does not need to concern themselves with it when using the method.

So far all the methods we have used have been ready-made Java methods. Next we will learn to create our own methods.