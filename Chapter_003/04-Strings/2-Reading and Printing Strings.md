You can read a string using the nextLine-method offered by Scanner. The program below reads the name of the user and prints it:
```Java
Scanner reader = new Scanner(System.in);

System.out.println("What's your name?");
// reading a line from the user and assigning it to the name variable
String name = reader.nextLine();
```

```Java
What's your name? Vicky 
Vicky
```

Strings can also be concatenated. If you place a `+`-operator between two strings, you get a new string that's a combination of those two strings. Be mindful of any white spaces in your variables!

```Java
String greeting = "Hi ";
String name = "Lily ";
String goodbye = " and see you later!";

String phrase = greeting + name + goodbye;
System.out.println(phrase);
```

```Java
Hi Lily and see you later!
```

![[Pasted image 20241028232253.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    // Write your program here
    
    // My Solution  
    System.out.println("Give a word: ");  
    String input = scanner.nextLine();  
  
    System.out.print(input);  
    System.out.print(input);  
    System.out.print(input);    
}
```

```Java
// Recommended Solution
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    // Write your program here  
  
    System.out.print("Give a word: ");  
    String word = scanner.nextLine();  
  
    System.out.println(""); // empty line  
    System.out.println(word + word + word);  
}
```

