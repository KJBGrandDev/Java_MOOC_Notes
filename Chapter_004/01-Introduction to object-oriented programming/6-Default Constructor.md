If the programmer does not define a constructor for a class, Java automatically creates a default one for it. A default constructor is a constructor that doesn't do anything apart from creating the object. The object's variables remain uninitialized (generally, the value of any object references will be `null`, meaning that they do not point to anything, and the values of primitives will be `0`)

For example, an object can be created from the class below by making the call `new Person()`

```Java
public class Person{
	private String name;
	private int age;
}
```

If a constructor has been defined for a class, no default constructor exists. For the class below, calling `new Person` would cause an error, as Java cannot find a constructor in the class that has no parameters.

```Java
public class Person{
	private String name;
	private int age;

	public Person(String initialName){
		this.age = 0;
		this.name = initialName;
	}
}
```