**A method** means a named set consisting of statements that can be called from elsewhere in the program code by its name. Programming languages offer pre-made methods, but programmers can also write their own ones. It would, in fact, be quite exceptional if a program used no methods written by the programmer, because methods help in structuring the program. From this point onward nearly every program on the course will therefore contain custom-created methods.

In the code boilerplate, methods are written outside of the curly braces of the `main`, yet inside out the "outermost" curly braces. They can be located above or below the main.

```java
import java.util.Scanner;

public class Example {
    public static void main(String[] args) {
        Scanner scanned = new Scanner(System.in);
        // program code
    }

    // your own methods here
}
```

Let's observe how to create a new method. We'll create the method `greet`

```Java
public static void greet(){
	System.out.println("Greetings from the method world!");
}
```

And then we'll insert it into a suitable place for a method.

```java
import java.util.Scanner;

public class Example {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // program code
    }

    // your own methods here
    public static void greet() {
        System.out.println("Greetings from the method world!");
    }
}
```

The definition of the method consists of two parts. The first line of the definition includes the name of the method, i.e. `greet`. On the left side of the name are the keywords `public static void`. Beneath the line containing the name of the method is a code block surrounded by curly brackets, inside of which is the code of the method — the commands that are executed when the method is called. The only thing our method `greet` does is write a line of text on the screen.

Calling a custom method is simple: write the name of the methods followed by a set of parentheses and the semicolon. In the following snippet the main program (main) calls the greet method four times in total.

```java
import java.util.Scanner;

public class ProgramStructure {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // program code
        System.out.println("Let's try if we can travel to the method world:");
        greet();

        System.out.println("Looks like we can, let's try again:");
        greet();
        greet();
        greet();
    }

    // own methods
    public static void greet() {
        System.out.println("Greetings from the method world!");
    }
}
```

The execution of the program produces the following output:

```Java
Let's try if we can travel to the method world: 
Greetings from the method world! 
Looks like we can, let's try again: 
Greetings from the method world! 
Greetings from the method world! 
Greetings from the method world!
```

The order of execution is worth noticing. The execution of the program happens by executing the lines of the main method (`main`) in order from top to bottom, one at a time. When the encountered statement is a method call, the execution of the program moves inside the method in question. The statements of the method are executed one at a time from top to bottom. After this the execution returns to the place where the method call occurred, and then proceeds to the next statement in the program.

Strictly speaking, the main program (`main`) itself is a method. When the program starts, the operating system calls `main`. The main method is the starting point for the program, since the execution begins from its first line. The execution of a program ends at the end of the main method.

![[Pasted image 20240908232440.png]]

![[Pasted image 20240908232656.png]]

From here on out, when introducing methods, we will not explicitly mention that they must be located in the correct place. Methods cannot be defined e.g. inside other methods.

## On Naming Methods

The names of methods begin with a word written entirely with lower-case letters, and the rest of the words begin with an upper-case letter - this style of writing is known as camelCase. Additionally, the code inside methods is indented by four characters.

In the code example below the method is poorly named. It begins with an upper-case letter and the words are separated by _ characters. The parentheses after the method name have a space between and indentation in the code block is incorrect.

```java
public static void This_method_says_woof ( ) {
System.out.println("woof");
}
```

In contrast the method below is correctly named: The name begins with a lower-case letter and the words are joined together with the camelCase style, meaning that each word after the first begins with an upper-case letter. The parentheses sit next to one another and the contents are correctly indented (the method has its own code block, so the indentation of the code is four characters).

```java
public static void thisMethodSaysWoof() {
    System.out.println("woof");
}
```