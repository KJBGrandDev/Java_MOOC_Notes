The next example demonstrates the addition of a few strings into an ArrayList containing strings. Addition is done with the list method `add`, which takes the value to be added as a parameter. We then print the value at position zero. To retrieve a value from a certain position, you use the list method `get`, which is given the place of retrieval as a parameter.

To call a list method you first write the name of the variable describing the list, followed by a dot and the name of the method.

```Java
//import the ArrayList so that the program can use it
import java.util.ArrayList;

public class program{
	public static void main(String[] args){
		//create the word list for storing strings
		ArrayList<String> wordList = new ArrayList<>();

		//add two values to the word list
		wordList.add("First");
		wordList.add("Second");

		//retrieve the value from position 0 of the word list, and print it
		System.out.println(wordList.get(0));
	}
}
```

```Java
First
```

As can be seen, the `get` method retrieves the first value from the list when it is given the parameter `0`. This is because **list positions are counted starting from zero**. The first value is found by `wordList.get(0)`, the second by `wordList.get(1)`, and so on.

```Java
import java.util.ArrayList;

public class program{
	public static void main(String[] args){
		ArrayList<String> wordList = new ArrayList<>();
		wordList.add("First");
		wordList.add("Second");
		System.out.println(wordList.get(1));
	}
}
```

```Java
Second
```

![[Pasted image 20241006233444.png]]

![[Pasted image 20241006233506.png]]