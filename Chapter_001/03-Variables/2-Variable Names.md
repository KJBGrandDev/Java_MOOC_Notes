Variable names are unique - no two variables can have the same name. The program in the following example is faulty as it attempts to create the variable "pi" twice.

The variable is created the first time its declared.
```Java
public class Program{
	public static void main(String[] args){
		double pi = 3.14;
		double pi = 3.141592653;

		System.out.println("The value of pi is: " + pi);
	}
}
```

The variable type is stated when the variable is first declared. When a new value is assigned to a variable, the type is no longer declared.
```Java
int value = 10;
System.out.println(value);
value = 4;
System.out.println(value);
```