In the example and exercise below, the required information was entered line by line. By no means is it impossible to ask for input in a specific format, e.g. separated by a comma.

If the name and age were separated by a comma, the program could work in the following manner.

```Java
Scanner scanner = new Scanner(System.in);
ArrayList<Person> persons = new ArrayList<>();

// Read person information from the user
System.out.println("Enter the person details separated by a comma, e.g.: Randall,2");
while(true){
	System.out.println("Enter the details, empty will stop: ");
	String details = scanner.nextLine();
	if(details.isEmpty()){
		break;
	}

	String[] parts = details.split(",");
	String name = parts[0];
	int age = Integer.valueOf(parts[1])
	persons.add(new Person(name, age));
}

// Print the number of the entered persons, and the person themselves
System.out.println();
System.out.println("Total number of persons: " + persons.size());
System.out.println("Persons: );

for( Person person: persons){
	System.out.println(person);
}
```

```Java
Enter the person details separated by a comma, e.g.: Randall,2 
Enter the details, empty will stop: **Leevi,2** 
Enter the details, empty will stop: **Anton,2** 
Enter the details, empty will stop: **Sylvi,0** 
Enter the details, empty will stop:

Total number of persons: 3 
Persons: 
Leevi, age 2 years 
Anton, age 2 years 
Sylvi, age 0 years
```