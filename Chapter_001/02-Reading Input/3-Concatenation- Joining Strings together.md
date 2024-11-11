The string to be printed can be formed from multiple strings using the " + " operator.

For example, the program below prints "Hello World!" on one line.
```Java
public class Program{
	public static void main(String[] args){
		System.out.println("Hello" + "World!");
	}
}
```

The same method can be used to join a "string literal" and the value of a "string variable"
```Java
public class Program{
	public static void main(String[] args){
		String message = "Hello World!";
		System.out.println(message + "...and the Universe!");
	}
}
```

We can do same with any number of strings.
```Java
public class Program{
	public static void main(String[] args){
		String start = "My name is ";
		String end = ", James Bond";

	System.out.println(start + "Bond" + end);
	//My name is Bond, James Bond
	}
}
```