The user input is read in string form. If we wanted to handle the input as integers, for instance, we'd have to convert it to another form. An example program has been provided below - it reads input from the user until the user inputs "end". As long as the user input is not "end" the inputs are handled as integers — in this case, the number is simply printed.

```Java
Scanner scanner = new Scanner(System.in);

while(true){
	String row = scanner.nextLine();

	if(row.equals("end")){
		break;
	}

	int number = Integer.valueOf(row);
	System.out.println(row)
}
```