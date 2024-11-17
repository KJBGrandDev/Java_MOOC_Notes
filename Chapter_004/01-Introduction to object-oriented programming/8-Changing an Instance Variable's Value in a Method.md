Let's add a method to the previously created person class that increments the age of the person by a year.

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

	//growOlder() method has been added
	public void growOlder(){
		this.age = this.age + 1;
	}
}
```

The method is written inside the `Person` class just as the `printPerson` method was. The method increments the value of the instance variable `age` by one.

The class diagram also gets an update.

![](https://i.imgur.com/LrUt8qg.png)

Let's call the method and see what happens:

```Java
public class Main{
	public static void main(String[] args){
		Person ada = new Person("Ada");
		Person antti = new Person("Antti");

		ada.printPerson();
		antti.printPerson();
		System.out.println("");

		ada.growOlder();
		ada.growOlder();

		ada.printPerson();
		antti.printPerson();
	}
}
```

The program's print output is as follows:

```Java
Ada, age 0 years 
Antti, age 0 years

Ada, age 2 years 
Antti, age 0 years
```

That is to say that when the two objects are "born" they're both zero-years old (`this.age = 0;` is executed in the constructor). The `ada` object's `growOlder` method is called twice. As the print output demonstrates, the age of Ada is 2 years after growing older. Calling the method on an object corresponding to Ada has no impact on the age of the other person object since each object instantiated from a class has its own instance variables.

The method can also contain conditional statements and loops. The growOlder method below limits aging to 30 years.

```Java
public class Person{
	private String name;
	private int age;

	public Person(String initialName){
		this.age = 0;
		this.name = initialName;
	}

	public void printPerson(){
		System.out.println(this.name + " , age " + this.age + " years");
	}

	// no one exceeds the age of 30
	public void growOlder(){
		if(this.age < 30){
			this.age = this.age + 1;
		}
	}
}
```