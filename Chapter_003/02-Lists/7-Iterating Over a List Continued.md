Let's make a new version of the program that prints each index manually. In this intermediate version we use the **index** variable to keep track of the place that is to be outputted.
```java
ArrayList<String> teachers = new ArrayList<>();

teachers.add("Simon");
teachers.add("Samuel");
teachers.add("Ann");
teachers.add("Anna");

int index = 0;

if (index < teachers.size()) {
    System.out.println(teachers.get(index)); // index = 0
    index = index + 1; // index = 1
}

if (index < teachers.size()) {
    System.out.println(teachers.get(index)); // index = 1
    index = index + 1; // index = 2
}

if (index < teachers.size()) {
    System.out.println(teachers.get(index)); // index = 2
    index = index + 1; // index = 3
}

if (index < teachers.size()) {
    System.out.println(teachers.get(index)); // index = 3
    index = index + 1; // index = 4
}

if (index < teachers.size()) {
    // this will not be executed since index = 4 and teachers.size() = 4
    System.out.println(teachers.get(index));
    index = index + 1;
}
```

We can see that there's repetition in the program above.

We can convert the `if` statements into a `while` loop that is repeated until the condition `index < teachers.size()` no longer holds (i.e., the value of the variable `index` grows too great).

Now the printing works regardless of the number of elements.

The for-loop we inspected earlier used to iterate over a known number of elements is extremely handy here. We can convert the loop above to a `for`-loop, after which the program looks like this.

```Java
ArrayList<String> teachers = new ArrayList<>();

teachers.add("Simon");
teachers.add("Samuel");
teachers.add("Ann");
teachers.add("Anna");

for(int index = 0; index < teachers.size(); index++){
	System.out.println(teachers.get(index));
}
```

```Java
Simon 
Samuel 
Ann 
Anna
```

The index variable of the for-loop is typically labelled `i`:

```Java
for(int i = 0; i < teachers.size(); i++){
	System.out.println(teachers.get(i));
}
```

Let's consider using a list to store integers. The functionality is largely the same as in the previous example. The greatest difference has to do with the initialization of the list — the type of value to be stored is defined as `Integer`, and the value to be printed is stored in a variable called `number` before printing.

```Java
ArrayList<Integer> numbers = new ArrayList<>();

numbers.add(1);
numbers.add(2);
numbers.add(3);
numbers.add(4);

for(int i = 0; i < numbers.size(); i++){
	System.out.println(numbers.get(i));
}
```

```Java
1
2
3
4
```

Printing the numbers in the list in reverse order would also be straightforward.
```java
ArrayList<Integer> numbers = new ArrayList<>();

numbers.add(1);
numbers.add(2);
numbers.add(3);
numbers.add(4);

int index = numbers.size() - 1;
while (index >= 0) {
    int number = numbers.get(index);
    System.out.println(number);
    index = index - 1;
}
```

```Java
ArrayList<Integer> numbers = new ArrayList<>();

numbers.add(1);
numbers.add(2);
numbers.add(3);
numbers.add(4);

for(int i = numbers.size - 1; i >= 0; i--){
	System.out.println(teachers.get(i));
}
```

```Java
4
3
2
1
```

![[Pasted image 20241007232017.png]]
![[Pasted image 20241007232031.png]]

![[Pasted image 20241013002940.png]]

![[Pasted image 20241013003012.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    ArrayList<Integer> numbers = new ArrayList<>();  
    int index = 0;  
    while (true) {  
        int size = numbers.size() - 1;  
        int luku = Integer.valueOf(scanner.nextLine());  
        if (luku == -1) {  
            break;  
        }  
  
        numbers.add(luku);  
    }
    //My solution
    while(index < numbers.size()) {  
        int number = numbers.get(index);  
        System.out.println(number);  
        index++;  
    }  
}
```

![[Pasted image 20241013003402.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    ArrayList<Integer> numbers = new ArrayList<>();  
    while (true) {  
        int number = Integer.valueOf(scanner.nextLine());  
        if (number == -1) {  
            break;  
        }  
  
        numbers.add(number);  
    }  
    //My solution
    System.out.println("From where? ");  
    int start = Integer.valueOf(scanner.nextLine());  
    System.out.println("To where? ");  
    int end = Integer.valueOf(scanner.nextLine());  
    for(int i = start; i <= end; i++){  
        System.out.println(numbers.get(i));  
    }  
}
```

```Java
//Best Solution
System.out.print("From where? ");
int lowerLimit = Integer.valueOf(scanner.nextLine());
System.out.print("To where? ");
int upperLimit = Integer.valueOf(scanner.nextLine());

while (lowerLimit <= upperLimit) {
	int number = numbers.get(lowerLimit);
	System.out.println(number);
	lowerLimit = lowerLimit + 1;
```

![[Pasted image 20241014001133.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    ArrayList<Integer> list = new ArrayList<>();  
    while (true) {  
        int input = Integer.valueOf(scanner.nextLine());  
        if (input == -1) {  
            break;  
        }  
  
        list.add(input);  
    }  
  
    System.out.println("");  
  
    //My Solution 
    int greatestNum = list.get(0);  
    for(int i = 0; i < list.size(); i++){  
        if(list.get(i) > greatestNum){  
            greatestNum = list.get(i);  
        }  
    }  
    System.out.println("The greatest number: " + greatestNum);  
}
```

```Java
// Best Solution
int biggest = list.get(0);
int index = 0;
while (index < list.size()) {
	if(biggest < list.get(index)) {
	biggest = list.get(index);
	}

	index++;
}
System.out.println("The greatest number: " + biggest);
```

![[Pasted image 20241015000549.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    ArrayList<Integer> list = new ArrayList<>();  
    while (true) {  
        int input = Integer.valueOf(scanner.nextLine());  
        if (input == -1) {  
            break;  
        }  
  
        list.add(input);  
    }  
  
    System.out.println("");  
  
    // implement here finding the indices of a number  
    System.out.println("Search for? ");  
    int searchNumber = Integer.valueOf(scanner.nextLine());  
    for(int i = 0; i < list.size(); i++){  
        if(searchNumber == list.get(i)){  
            System.out.println(searchNumber + " is at index " + i);  
        }  
    }  
}
```

```Java
// implement here finding the indices of a number  
System.out.print("Search for? ");  
int searching = Integer.valueOf(scanner.nextLine());  
  
int index = 0;  
    while (index < list.size()) {  
    if (list.get(index) == searching) {  
        System.out.println(searching + " is at index " + index);  
    }  
  
    index++;
```

![[Pasted image 20241015001530.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    // implement here a program that reads user input  
    // until the user enters 9999    ArrayList<Integer> list = new ArrayList<>();  
    while(true){  
        int input = Integer.valueOf(scanner.nextLine());  
        if(input == 9999){  
            break;  
        }  
        list.add(input);  
    }  
  
    // after that, the program prints the smallest number  
    // and its index -- the smallest number    
    // might appear multiple times    int smallestNum = list.get(0);

	// My Solution
    int smallestNumIndex = 0;  
    int i = 0;  
    while(i < list.size()){  
        if(smallestNum > list.get(i)){  
            smallestNum = list.get(i);  
            smallestNumIndex = i;  
        }  
        i++;  
    }  
    System.out.println("Smallest number: " + smallestNum);  
    System.out.println("Found at index: " + smallestNumIndex);  
}
```

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    // implement here a program that reads user input  
    // until the user enters 9999  
    // after that, the program prints the smallest number    
    // and its index -- the smallest number    
    // might appear multiple times    ArrayList<Integer> list = new ArrayList<>();  
    while (true) {  
        int input = Integer.valueOf(scanner.nextLine());  
        if (input == 9999) {  
            break;  
        }  
        list.add(input);  
    }  
  
    System.out.println("");

	//Recommended Solution
  
    int smallest = list.get(0);  
    int index = 0;  
    while (index < list.size()) {  
        if (list.get(index) < smallest) {  
            smallest = list.get(index);  
        }  
  
        index++;  
    }  
  
    System.out.println("Smallest number: " + smallest);  
  
    index = 0;  
    while (index < list.size()) {  
        if (list.get(index) == smallest) {  
            System.out.println("Found at index: " + index);  
        }  
        index++;  
    }  
}
```