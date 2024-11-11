Strings can't be compared with with the equals operator - `==`. For strings, there exists a separate `equals`-command, which is always appended to the end of the string that we want to compare.

```Java
String text = "course";

if(text.equals("marzipan")){
	System.out.println("The text variable contains the text marzipan.");
} else {
	System.out.println("The text variable does not contain the text marzipan.");
}
```

The `equals` command is always appended to the end of the string that we want to compare, "string variable dot equals some text". You can also compare a string variable to another string variable.

```Java
String text = "course";
String anotherText = "horse";

if(text.equals(anotherText)){
	System.out.println("The two texts are equal!");
} else {
	System.out.println("The two texts are not equal!");
}
```

When comparing strings, you should make sure the string variable has some value assigned to it. If it doesn't have a value, the program will produce a _NullPointerException_ error, which means that no value has been assigned to the variable, or that it is empty (_null_).

As we've come to know, a boolean value can be inverted through negation - `!`.

```Java
System.out.println("Make sure the text is not 'cake'");
String text = "pie";

if(!(text.equals("cake"))){
	System.out.println("It wasn't!");
} else {
	System.out.println("It was!");
}
```

```Java
It wasn't!
```

![[Pasted image 20241028233143.png]]

```Java
// My Solution
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
    System.out.println("Give a string: ");  
    String input = scanner.nextLine();  
  
    String condition = "true";  
    if(!(input.equals(condition))){  
        System.out.println("Try again!");  
    } else {  
        System.out.println("You got it right!");  
    }  
}
```

```Java
// Recommended Solution
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    System.out.print("Give a string: ");  
    String string = scanner.nextLine();  
  
    if (string.equals("true")) {  
        System.out.println("You got it right!");  
    } else {  
        System.out.println("Try again!");  
    }  
}
```

![[Pasted image 20241028233644.png]]
![[Pasted image 20241028233658.png]]
![[Pasted image 20241028233712.png]]

```Java
// My Solution
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    System.out.println("Enter username: ");  
    String username = scanner.nextLine();  
  
    System.out.println("Enter password: ");  
    String password = scanner.nextLine();  
  
    loggingIn(username, password);  
}  
public static void loggingIn(String username, String password){  
    String[] firstAccount = {"alex","sunshine"};  
    String[] secondAccount = {"emma","haskell"};  
  
    if(firstAccount[0].equals(username) && firstAccount[1].equals(password)){  
        System.out.println("You have successfully logged in!");  
    } else if(secondAccount[0].equals(username) && secondAccount[1].equals(password)){  
        System.out.println("You have successfully logged in!");  
    } else {  
        System.out.println("Incorrect username or password!");  
    }  
  
}
```

```Java
// Recommended Solution
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    System.out.print("Enter username: ");  
    String username = scanner.nextLine();  
    System.out.print("Enter password: ");  
    String password = scanner.nextLine();  
  
    // NB! This is an aweful way to get it done. If there were more users  
    // the code would get really messy. We'll learn a better way soon!    
    if ((username.equals("alex") && password.equals("sunshine")) ||(username.equals("emma") && password.equals("haskell"))) {  
        System.out.println("You have successfully logged in!");  
    } else {  
        System.out.println("Incorrect username or password!");  
    }  
}
```

