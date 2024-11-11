You can use arrays as a parameter of a method just like any other variable. As an array is a reference type, the value of the array is a reference to the information contained in the array. When you use array as a parameter of a method, the method receives a copy of the reference to the array.

```Java
public static void listElements(int[] integerArray){
	System.out.println("the elements of the array are: ");
	int index = 0;
	while(index < integgerArray.length){
		int number = integerArray[index];
		System.out.print(number + " ");
		index = index + 1;
	}
	System.out.println("");
}
```

```Java
int[] numbers = new int[3];
numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;

listElements(numbers);
```

```Java
the elements of the array are: 1 2 3
```

As noticed earlier, you can freely choose the name of the parameter inside the method, the name doesn't have to be the same as the name of the variable when you call the method. In the example above, we call the array `integerArray`, meanwhile the caller of the method has named the same array `numbers`.

Array is an object, so when you change the array inside the method, the changes persist after the execution of the method.

![[Pasted image 20241027175928.png]]

```Java
public static void main(String[] args) {
        // You can try the method here
        int[] array = {5, 1, 3, 4, 2};
        System.out.println(sumOfNumbersInArray(array));
    }

    public static int sumOfNumbersInArray(int[] array) {
        // Write some code here
        
		// My Solution
        int index = 0;
        int sum = 0;
        while(index < array.length){
            sum = sum + array[index];
            index++;
        }
        return sum;
    }
```

```Java
// Recommended Solution
public static int sumOfNumbersInArray(int[] array) {
    // Write some code here
    int sum = 0;
    for (int num : array) {
        sum = sum + num;
    }
    return sum;
}
```

![[Pasted image 20241028005443.png]]

```Java
public static void main(String[] args) {  
    // You can test your method here  
    int[] array = {5, 1, 3, 4, 2};  
    printNeatly(array);  
}  
  
public static void printNeatly(int[] array) {  
    // Write some code in here
    
    // My Solution 
    int index = 0;  
    while(index < array.length){  
        if(index == array.length - 1){  
            System.out.println(array[index]);  
        } else {  
            System.out.print(array[index] + ", ");  
        }  
        index++;  
    }  
}
```

```Java
// Recommended Solution
public static void printNeatly(int[] array) {
    // Write some code in here
    int index = 0;
    while (index < array.length) {
        System.out.print(array[index]);
        if (index < (array.length - 1)) {
            System.out.print(", ");
        }
 
        index = index + 1;
    }
    System.out.println();
}
```

![[Pasted image 20241028013537.png]]

```Java
public static void main(String[] args) {  
    // You can test the method here  
    int[] array = {5, 1, 3, 4, 2};  
    printArrayInStars(array);  
}  
  
public static void printArrayInStars(int[] array) {  
    // Write some code in here
    
    // My Solution  
    int index = 0;  
    int starsCount = 0;  
    while(index < array.length){  
        while(starsCount < array[index]){  
            System.out.print("*");  
            starsCount++;  
        }  
        System.out.println("");  
        index++;  
        starsCount = 0;  
    }  
}
```

```Java
// Recommended Solution
public static void printArrayInStars(int[] array) {
    // Write some code in here
    for (int stars : array) {
        printStars(stars);
        System.out.println();
    }
}
 
public static void printStars(int howMany) {
    while (howMany > 0) {
        System.out.print("*");
        howMany = howMany - 1;
    }
}
```