We've been using the `Scanner`-class since the beginning of this course to read user input. The block in which data is read has been a while-true loop where the reading ends at a specific input.

```Java
Scanner scanner = new Scanner(System.in);

while(true){
	String line = scanner.nextLine();

	if(line.equals("end")){
		break;
	}

	// add the read line to a list for later
	// handling or handle the line immediately
}
```

In the example above, we pass system input (`System.in`) as a parameter to the constructor of the Scanner-class. In text-based user interfaces, the input of the user is directed into the input stream one line at a time, which means that the information is sent to be handled every time the user enters a new line.