Splitting strings is used particularly when the data is of a fixed format. This refers to data that adheres to some predefined format. An example of this of this is the comma-separated values (`csv`) format, where commas are used to separate values. Below you'll find an example of data in csv form containing names and ages. The first column contains names and the second one ages. The columns are separated by a comma.

```Java
sebastian,2 
lucas,2 
lily,1
```

Let's assume the user enters the data above row by row, ending with an empty line.

A program to print the names and ages looks like the following:

```Java
Scanner reader = new Scanner(System.in);

while(true){
	String input = reader.nextLine();
	if(input.equals("")){
		break;
	}

	String[] pieces = input.split(",");
	System.out.println("Name: " + pieces[0] + ", age: " + pieces[1]);
}
```

```Java
sebastian,2
Name: sebastian, age: 2

lucas,2 
Name: lucas, age: 2

lily,1 
Name: lily, age: 1
```

![[Pasted image 20241109005432.png]]

```Java
public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        while(true){
            String input = scanner.nextLine();
            if(input.equals("")){
                break;
            }

            String[] pieces = input.split(" ");
            System.out.println(pieces[0]);
        }
    }
```

![[Pasted image 20241109011115.png]]

```Java
public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);

        while(true){
            String input = scanner.nextLine();
            if(input.equals("")){
                break;
            }

            String[] pieces = input.split(" ");
            int lastNumber = pieces.length - 1;
            System.out.println(pieces[lastNumber]);
        }
    }
```
