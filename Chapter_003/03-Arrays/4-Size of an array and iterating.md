You can find the size of the array through the associated variable `length`. You can access this associated variable by writing name of the array dot name of the variable, i.e. `numbers.length`. Note, that this is not a method call, so `numbers.length()` doesn't work.

You can iterate over the array, i.e. go through each element of the array with a while loop.

```Java
int[] numbers = new int[4];
numbers[0] = 42;
numbers[1] = 13;
numbers[2] = 12;
numbers[3] = 7;

System.out.println("The array has " + numbers.length + " elements.");

int index = 0;
while(index < numbers.length){
	System.out.println(numbers[index]);
	index = index + 1 //index += 1
}
```

```Java
The array has 4 elements. 
42 
13 
12 
7
```

The example above iterates over indices 0, 1, 2 and 3, and at each index prints the value held in the index. So first it prints `numbers[0]`, then `numbers[1]` etc. The iteration stops, once the condition of the loop `index < number.length` is false, i.e. once the index variable is greater or equal to the length of the array. NB! The iteration doesn't stop the moment the index variable grows too big; the condition is evaluated only in the beginning of the while loop.

![[Pasted image 20241026231653.png]]

```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
    int[] array = new int[10];  
    array[0] = 6;  
    array[1] = 2;  
    array[2] = 8;  
    array[3] = 1;  
    array[4] = 3;  
    array[5] = 0;  
    array[6] = 9;  
    array[7] = 7;  
  
    System.out.print("Search for? ");  
    int searching = Integer.valueOf(scanner.nextLine());  
  
    // Implement the search functionality here  
    int index = 0;  
    while(index <= array.length){  
        if(array[index] == searching){  
            System.out.println(searching + " is at index " + index + ".");  
            break;  
        }  
        if(index == array.length -1 && array[index] != searching){  
            System.out.println(searching + " was not found.");  
            break;  
        }  
        index++;  
    }  
}
```

```Java
//recommended solution
int index = 0;  
boolean found = false;  
while (index < array.length) {  
    if (array[index] == searching) {  
        System.out.println(searching + " is at index " + index + ".");  
        found = true;  
    }  
   
    index++;  
}  
   
if (!found) {  
    System.out.println(searching + " was not found.");  
}
```

<mark class="hltr-yellow">If the index is pointing outside the Array, i.e. the element doesn't exist, we get an</mark> **ArrayIndexOutOfBoundsException**. This error tells, that the Array doesn't contain the given index. You cannot access outside of the Array, i.e. index that's less than 0 or greater or equal to the size of the Array.

The next example is a program that initially asks the user to enter how many numbers, and then enter the numbers. Finally it prints back the numbers in the same order. The numbers are stored in an Array.

```Java
System.out.println("How many numbers? ");
int howMany = Integer.valueOf(reader.nextLine());

int[] numbers = new int[howMany];

System.out.println("Enter the numbers:");

int index = 0;
while(index < numbers.length){
	numbers[index] = Integer.valueOf(reader.nextLine());
	index = index + 1;
}

System.out.println("Here are the numbers again:");
index = 0;
while(index < numbers.length{
	System.out.println(numbers[index]);
	index = index + 1;
}
```

An execution of the program might look like this:
```Java
How many numbers? 4
Enter the numbers: 
4
8
2 
1 
Here are the numbers again: 
4 
8 
2 
1
```