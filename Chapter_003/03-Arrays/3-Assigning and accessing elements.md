An element of an Array is referred to by its index. In the example below we create an Array to hold 3 integers, and then assign values to indices 0 and 2. After that we print the values.

```Java
int[] numbers = new int[3];
numbers[0] = 2;
numbers[2] = 5;

System.out.println(numbers[0]);
System.out.println(numbers[2]);
```

Assigning a value to a specific spot of an Array works much like assigning a value in a normal variable, but in the Array you must specify the index, i.e. to which spot you want to assign the value. The index is specified in square brackets. The ArrayList `get`-method works very similarly to accessing an element of an Array. Just the syntax, i.e. the way things are written, is different.

The index is an integer, and its value is between [0, length of the Array - 1]. For example an Array to hold 5 elements has indices 0, 1, 2, 3, and 4.

```Java
Scanner reader = new Scanner(System.in);

int[] numbers = new int[5];
numbers[0] = 42;
numbers[1] = 13;
numbers[2] = 12;
numbers[3] = 7;
numbers[4] = 1;

System.out.println("Which index should we access?");
int index = Integer.valueOf(reader.nextLine());

System.out.println(numbers[index]);
```

The value held in an Array can also be assigned to be the value of another variable.

```Java
Scanner reader = new Scanner(System.in);

int[] numbers = new int[5];
numbers[0] = 42;
numbers[1] = 13;
numbers[2] = 12;
numbers[3] = 7;
numbers[4] = 1;

System.out.println("Which index should we access?");
int index = Integer.valueOf(reader.nextLine());

int number = numbers[index];
System.out.println(number);
```

![[Pasted image 20241026223156.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
    int[] array = new int[5];  
    array[0] = 1;  
    array[1] = 3;  
    array[2] = 5;  
    array[3] = 7;  
    array[4] = 9;  
  
    int index = 0;  
    while (index < array.length) {  
        System.out.println(array[index]);  
        index++;  
    }  
    System.out.println("");  
  
    // Implement here  
    // asking for the two indices    
    // and then swapping them

    // my solution
    System.out.println("Give two indices to swap:");  
    int firstInput = Integer.valueOf(scanner.nextLine());  
    int secondInput = Integer.valueOf(scanner.nextLine());  
  
    int swapInputHolder = array[firstInput];  
    array[firstInput] = array[secondInput];  
    array[secondInput] = swapInputHolder;  
  
    System.out.println("");  
    index = 0;  
    while (index < array.length) {  
        System.out.println(array[index]);  
        index++;  
    }  
}
```

```Java
//recommended solution
System.out.println("Give two indices to swap:");
int first = Integer.valueOf(scanner.nextLine());
int second = Integer.valueOf(scanner.nextLine());
 
int helper = array[first];
array[first] = array[second];
array[second] = helper;
////////////////////////////////////////////////////
System.out.println("");  
    index = 0;  
    while (index < array.length) {  
        System.out.println(array[index]);  
        index++; 
```
