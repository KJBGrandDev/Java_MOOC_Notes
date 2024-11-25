The structure we used earlier for reading inputs is still very useful.

```Java
Scanner scanner = new Scanner(System.in);
ArrayList<Person> persons = new ArrayList<>();

// Read the names of persons from the user
while(true){
	System.out.println("Enter a name, empty will stop: ");
	String name = scanner.nextLine();
	if(name.isEmpty()){
		break;
	}

	// Add to the list a new person
	// whose name is the previous user input
	persons.add(new Person(name));
}

// Print the number of the entered persons, and their individual information
System.out.println();
System.out.println("Persons in total: " + persons.size());
System.out.println("Persons: ");

for (Person person: persons){
	System.out.println(person);
}
```

```Java
Enter a name, empty will stop: Alan Kay 
Enter a name, empty will stop: Ivan Sutherland 
Enter a name, empty will stop: Kristen Nygaard

Persons in total: 3 
Persons: 
Alan Kay, age 0 years 
Ivan Sutherland, age 0 years 
Kristen Nygaard, age 0 years
```