We know how to create an object and initialize its variables. However, an object also needs methods to be able to do anything. As we've learned, a **method** is a named section of source code inside a class which can be invoked.

```Java
public class Person{
	private String name;
	private int age;

	public Person(String initialName){
		this.age = 0;
		this.name = initialName;
	}

	public void printPerson() {
		System.out.println(this.name + " , age " + this.age + " years");
	}
}
```

A method is written inside of the class beneath the constructor. The method name is preceded by `public void`, since the method is intended to be visible to the outside world (`public`), and it does not return a value (`void`).

![](https://i.imgur.com/HhJ1iG7.png)

In addition to the class name, instance variables and constructor, the class diagram now also includes the method `printPerson`. Since the method comes with the `public` modifier, the method name is prefixed with a plus sign. No parameters are defined for the method, so nothing is put inside the method's parentheses. The method is also marked with information indicating that it does not return a value, here `void`.

![](https://i.imgur.com/Vy4iLAK.png)

The method `printPerson` contains one line of code that makes use of the instance variables `name` and `age` — the class diagram says nothing about its internal implementations. Instance variables are referred to with the prefix `this`. All of the object's variables are visible and available from within the method.

Let's create three persons in the main program and request them to print themselves:

```Java
public class Main{
	public static void main(String[] args){
		Person ada = new Person("Ada");
		Person antti = new Person("Antii");
		Person martin = new Person("Martin");

		ada.printPerson();
		antti.printPerson();
		martin.printPerson();
	}
}
```

Prints:

```Java
Ada, age 0 years 
Antti, age 0 years 
Martin, age 0 years
```

