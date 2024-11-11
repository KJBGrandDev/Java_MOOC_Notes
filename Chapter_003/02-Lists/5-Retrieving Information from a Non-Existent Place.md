If you try to retrieve information from a place that does not exist on the list, the program will print a `IndexOutOfBoundsException` error. In the example below, two values are added to a list, after which there is an attempt to print the value at place two on the list.

```Java
import java.util.ArrayList;

public class Example{
	public static void main(String[] args){
		ArrayList<String> wordList = new ArrayList<>();
		wordList.add("First");
		wordList.add("Second");
		System.out.println(wordList.get(2));
	}
}
```

Since the numbering (i.e., **indexing**) of the list elements starts with zero, the program isn't able to find anything at place two and its execution ends with an error. Below is a description of the error message caused by the program.

```Java
Exception in thread "main" java.lang.IndexOutOfBoundsException: Index: 2, Size: 2 
at java.util.ArrayList.rangeCheck(ArrayList.java:653) 
at java.util.ArrayList.get(ArrayList.java:429) 
at Example.main(Example.java:(line)) 
Java Result: 1
```

The error message provides hints of the internal implementation of an ArrayList object. It lists all the methods that were called leading up to the error. First, the program called the `main` method, whereupon ArrayList's `get` method was called. Subsequently, the `get` method of ArrayList called the `rangeCheck` method, in which the error occurred. This also acts as a good illustration of proper method naming. Even if we'd never heard of the `rangeCheck` method, we'd have good reason to guess that it checks if a searched place is contained within a given desired range. The error likely occurred because this was not the case.

![[Pasted image 20241006235728.png]]

![[Pasted image 20241007000241.png]]

![[Pasted image 20241007000254.png]]
![[Pasted image 20241007000400.png]]

![[Pasted image 20241007000419.png]]
