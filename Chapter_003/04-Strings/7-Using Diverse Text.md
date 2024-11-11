We've printed strings in the examples above. Some of the data contained in a fixed-format string can be numerical. In the previous data we used that contained names and ages, the ages were integers.

```Java
sebastian,2 
lucas,2 
lily,1
```

Splitting a string always produces an array of strings. If the text is of fixed format, we can assume the data in a specific index to always be of the a specific type — e.g., in the example above, age at index 1 is an integer.

The program below computes the sum of ages in this fixed format data. In order to compute the sum, the age must first be converted to a number (the familiar command `Integer.valueOf()`)

```Java
Scanner reader = new Scanner(System.in);
int sum = 0;

while(true){
	String input = reader.nextLine();
	if(input.equals("")){
		break;
	}
	String[] parts = input.split(",");
	sum = sum + integers.valueOf(parts[1]);
}
System.out.println("Sum of the age is: " + sum);
```

```Java
sebastian,2 
lucas,2 
lily,1

Sum of the ages is 5
```

We can write a program to compute the average of the ages in the same way:

```Java
Scanner reader = new Scanner(System.in);
int sum = 0;
int count = 0;

while(true){
	String input = reader.nextLine();
	if(input.equals("")){
		break;
	}
	String[] parts = input.split(",");
	sum = sum + Integer.valueOf(parts[1]);
	count = count + 1;
}
if(count > 0){
	System.out.println("Age average: " + (1.0 * sum / count));
} else {
	System.out.println("No input");
}
```

```Java
sebastian,2 
lucas,2 
lily,1

Age average: 1.666
```

![](https://i.imgur.com/0LAOZTJ.png)

```Java
//My Solution
public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);

        int oldestAge = 0;

        while(true){
            String stringInput = scanner.nextLine();
            if(stringInput.equals("")){
                System.out.println("Age of the Oldest: " + oldestAge);
                break;
            }

            String[] stringArray = stringInput.split(",");
            int age = Integer.valueOf(stringArray[1]);
            
            if(age > oldestAge){
                oldestAge = age;
            }
        } 
    }
```

![](https://i.imgur.com/WmAIAma.png)

```Java
//My Solution
public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);

        String oldestPersonName = "";
        int oldestAge = 0;
        while(true){
            String input = scanner.nextLine();
            if(input.equals("")){
                System.out.println("Name of the oldest: " + oldestPersonName);
                break;
            }

            String[] stringArray = input.split(",");
            String name = stringArray[0];
            int age = Integer.valueOf(stringArray[1]);

            if(age > oldestAge){
                oldestAge = age;
                oldestPersonName = name;
            }
        }
    }
```

```Java
//Preferred Solution
public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
 
        int oldest = -1;
        String name = "";
 
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("")) {
                break;
            }
 
            String[] parts = input.split(",");
            int age = Integer.valueOf(parts[1]);
            if (age > oldest) {
                oldest = age;
                name = parts[0];
            }
        }
        
        System.out.println("Name of the oldest: " + name);
    }
```