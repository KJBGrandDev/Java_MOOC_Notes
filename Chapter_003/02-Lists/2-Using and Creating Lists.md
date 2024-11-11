For an ArrayList to be used, it first needs be imported into the program. This is achieved by including the command `import java.util.ArrayList;` at the top of the program. Below is an example program where an ArrayList is imported into the program.

```Java
import java.util.ArrayList;

public class program {
	public static void main(String[] args){
		//no implementation yet
	}
}
```

Creating a new list is done with the command `ArrayList<Type> list = new ArrayList<>()`, where _Type_ is the type of the values to be stored in the list (e.g. `String`). We create a list for storing strings in the example below.

```Java
// import the ArrayList so that the program can use it
import java.util.ArrayList;

public class program{
	public static void main(String[] args){
		//create a list
		ArrayList<String> list = new ArrayList<>();
		// the list isn't used yet
	}
}
```

The type of the ArrayList variable is `ArrayList`. When a list variable is initialized, the type of the values to be stored is also defined in addition to the variable type — **all the variables stored in a given list are of the same type**. As such, the type of an ArrayList that stores strings is `ArrayList<String>`. A new list is created with the command `new ArrayList<>();`.