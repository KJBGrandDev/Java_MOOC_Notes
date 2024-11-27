If the constructor demands more than one parameter, you can query the user for more information. Let's assume we have the following constructor for the class `Person`.

```Java
public class Person{
	private String name;
	private int age;
	private int weight;
	private int height;

	public Person(String name, int age){
		this.name = name;
		this.age = age;
		this.weight = 0;
		this.height = 0;
	}

	//Methods
}
```

In this case, an object is created by calling the two-parameter constructor.

If we want to query the user for this kind of object, they must be asked for each parameter separately. In the example below, name and age parameters are asked separately from the user. Entering an empty name will end the reading part.

The persons are printed after they have been read.

```Java
Scanner scanner = new Scanner(System.in);
ArrayList<Person> persons = new ArrayList<>();

// Read person information from the user
while(true){
	System.out.println("Enter name, empty will end: ");
	String name = scanner.nextLine();
	if(name.isEmpty()){
		break;
	}

	System.out.print("Enter the age of the person " + name + ": ");
	int age = Integer.valueOf(scanner.nextLine());

	//We add a new person to the list.
	//The person's name and age were decided by the user
	persons.add(new Person(name, age));
}

//We'll print the number of the inputted persons, and the persons themselves
System.out.println();
System.out.println("Total number of persons: " + persons.size());
System.out.println("Persons: ");

for(String person: persons){
	System.out.println(person);
}
```

```Java
Enter name, empty will end: **Grace Hopper** 
Enter the age of the person Grace Hopper: **85** 
Enter name, empty will end:

Total number of persons: 1 
Persons: 
Grace Hopper, age 85 years
```