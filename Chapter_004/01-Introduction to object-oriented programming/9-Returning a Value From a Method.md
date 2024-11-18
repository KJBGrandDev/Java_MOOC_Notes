A method can return a value. The methods we've created in our objects haven't so far returned anything. This has been marked by typing the keyword _void_ in the method definition.

```Java
public class Door{
	public void knock(){
		//...
	}
}
```

The keyword **void** means that the method does not return a value.

If we want the method to return a value, we need to replace the `void` keyword with the type of the variable to be returned. In the following example, the Teacher class has a method `grade` that always returns an integer-type (`int`) variable (in this case, the value 10). The value is always returned with the **return** command:

```Java
public class Teacher{
	public int grade(){
		return 10;
	}
}
```

The method above returns an `int` type variable of value 10 when called. For the return value to be used, it needs to be assigned to a variable. This happens the same way as regular value assignment, i.e., by using the equals sign:

```Java
public static void main(String[] args){
	Teacher teacher = new Teacher();

	int grading = teacher.grade();

	System.out.println("The grade received is: " + grading);
}
```

```Java
The grade received is 10
```

The method's return value is assigned to a variable of type `int` value just as any other int value would be. The return value could also be used to form part of an expression.

```Java
public static void main(String[] args){
	Teacher first = new Teacher();
	Teacher second = new Teacher();
	Teacher third = new Teacher();

	double average = (first.grade()) + second.grade() + third.grade()) / 3.0;

	System.out.println("Grading average: " + average);
}
```

```Java
Grading average 10.0
```

All the variables we've encountered so far can also be returned by a method. To sum:

- A method that returns nothing has the `void` modifier as the type of variable to be returned.

```Java
public void methordReturnsNothing(){
	// the method body
}
```

- A method that returns an integer variable has the `int` modifier as the type of variable to be returned.

```Java
public int methodThatReturnsAnInteger(){
	// the method body, requires a return statement
}
```

- A method that returns a string has the `String` modifier as the type of the variable to be returned

```Java
public String methodThatReturnsAString(){
	// the method body, requires a return statement
}
```

- A method that returns a double-precision number has the `double` modifier as the type of the variable to be returned.

```Java
public double methodThatReturnsADouble(){
	// the method body, requires a return statement
}
```

Let's continue with the Person class and add a `returnAge` method that returns the person's age.

```Java
public class Person{
	private String name;
	private int age;

	public Person(String initialName){
		this.age = 0;
		this.name = initialName;
	}

	public void printPerson(){
		System.out.println(this.name + ", age " + this.age + " years");
	}

	public void growOlder(){
		if(this.age < 30){
			this.age = this.age + 1;
		}
	}

	// the added method
	public int returnAge(){
		return this.age;
	}
}
```

The class in its entirety:

![](https://i.imgur.com/3IzeRPt.png)


Let's illustrate how the method works:

```Java
public class Main{
	public static void main(String[] args){
		Person pekka = new Person("Pekka");
		Person antti = new Person("Antti");

		pekka.growOlder();
		pekka.growOlder();

		antti.growOlder();

		System.out.println("Pekka's age: " + pekka.returnAge());
		System.out.println("Antti's age: " + antti.returnAge());
		int combined = pekka.returnAge() + antti.returnAge();

		System.out.println("Pekka's and Antti's combined age " + combined + " years");
	}
}
```

```Java
Pekka's age 2 
Antti's age 1

Pekka's and Antti's combined age 3 years
```

