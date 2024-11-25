Strings are objects, so it should come as no surprise that other kinds of objects can also be found in lists. Next, let's examine the cooperation of lists and objects in more detail.

Let's assume we have access to the class defined below, describing a person.

```Java
public class Person{
	private String name;
	private int age;
	private int weight;
	private int height;

	public Person(String name){
		this.name = name;
		this.age = 0;
		this.weight = 0;
		this.height = 0;
	}

	public String getName(){
		return this.name;
	}

	public int getAge(){
		return this.age;
	}

	public void growOlder(){
		this.age = this.age + 1;
	}

	public void setHeight(int newHeight){
		this.height = newHeight;
	}

	public void setWeight(int newWeight){
		this.weight = newWeight;
	}

	public double bodyMassIndex(){
		double heightDivByHundred = this.height / 100.0;
		return this.weight / (heightDivByHundred * heightDivByHundred);
	}

	//Override
	public String toString(){
		return this.name + ", age " + this.age + " years";
	}
}
```

Handling objects in a list is not really different in any way from the previous experience we have with lists. The essential difference is only to define the type for the stored elements when you create the list.

In the example below we first create a list meant for storing Person type object, after which we add persons to it. Finally the person objects are printed one by one.

```Java
ArrayList<Person> persons = new ArrayList<>();

// a person object can be created first
Person john = new Person("John");
// and then added to the list
persons.add(john);

// person objects can also be created "in the same sentence" that they are added to the list
persons.add(new Person("Matthew"));
persons.add(new Person("Martin"));

for(Person person: persons){
	System.out.println(person);
}
```

```Java
John, age 0 years 
Matthew, age 0 years 
Martin, age 0 years
```