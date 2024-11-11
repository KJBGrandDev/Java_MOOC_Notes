Like other variables, a list can be used as a parameter to a method too. When the method is defined to take a list as a parameter, the type of the parameter is defined as the type of the list and the type of the values contained in that list. Below, the method `print` prints the values in the list one by one.

```Java
public static void print(ArrayList<String> list){
	for(String value: list){
		System.out.println(value);
	}
}
```

We're by now familiar with methods, and it works in the same way here. In the example below we use the `print` method that was implemented above.

```java
ArrayList<String> strings = new ArrayList<>();

strings.add("First");
strings.add("Second");
strings.add("Third");

print(strings);
```

```Java
First 
Second 
Third
```

The chosen parameter in the method definition is not dependent on the list that is passed as parameter in the method call. In the program that calls `print`, the name of the list variable is `strings`, but inside the method `print` the variable is called `list` — the name of the variable that stores the list could also be `printables`, for instance.

It's also possible to define multiple variables for a method. In the example the method receives two parameters: a list of numbers and a threshold value. It then prints all the numbers in the list that are smaller than the second parameter.

```Java
public static void printSmallerThan(ArrayList<Integer> numbers, int threshold){
	for(int number: numbers){
		if(number < threshold){
			System.out.println(number);
		}
	}
}
```

```Java
ArrayList<Integer> list = new ArrayList<>();

list.add(1);
list.add(2);
list.add(3);
list.add(2);
list.add(1);

printSmallerThan(list, 3);
```

```Java
1
2
2
1
```

![[Pasted image 20241024183159.png]]

```Java
public static void main(String[] args) {  
    // Try your method here  
ArrayList<Integer> numbers = new ArrayList<>();  
  
numbers.add(3);  
numbers.add(2);  
numbers.add(6);  
numbers.add(-1);  
numbers.add(5);  
numbers.add(1);  
  
System.out.println("The numbers in the range [0, 5]");  
printNumbersInRange(numbers, 0, 5);  
  
System.out.println("The numbers in the range [3, 10]");  
printNumbersInRange(numbers, 3, 10);  
}  
public static void printNumbersInRange(ArrayList<Integer> numbers, int lowerLimit, int upperLimit){  
    for(Integer list: numbers){  
        if(list >= lowerLimit && list <= upperLimit){  
            System.out.println(list);  
        }  
    }  
}
```

```Java
// recommended solution
public static void printNumbersInRange(ArrayList<Integer> numbers, int lowerLimit, int upperLimit) {  
    for (Integer number : numbers) {  
        if (number < lowerLimit) {  
            continue;  
        }  
  
        if (number > upperLimit) {  
            continue;  
        }  
  
        System.out.println(number);  
    }  
}
```

As before, a method can also return a value. The methods that return values have the type of the return value in place of the `void` keyword, and the actual returning of the value is done by the `return` command. The method below returns the size of the list.

```Java
public static int size(ArrayList<String> list){
	return list.size();
}
```

You can also define own variables for methods. The method below calculates the average of the numbers in the list. If the list is empty, it returns the number -1.

```Java
	public static double average(ArrayList<Integer> numbers){
		if(number.size() == 0){
			return -1;
		}
		int sum = 0;
		for(int number: numbers){
			sum = sum + number;
		}
		return 1.0 * sum / numbers.size();
	}
```

![[Pasted image 20241024190945.png]]

```Java
public static void main(String[] args) {  
    // Try your method here  
    ArrayList<Integer> numbers = new ArrayList<>();  
    numbers.add(3);  
    numbers.add(2);  
    numbers.add(6);  
    numbers.add(-1);  
    System.out.println(sum(numbers));  
  
    numbers.add(5);  
    numbers.add(1);  
    System.out.println(sum(numbers));  
}  
//my solution
public static int sum(ArrayList<Integer> numbers){  
    int sum = 0;  
    for(Integer list: numbers){  
        sum = sum + list;  
    }  
    return sum;  
}
```

```Java
public static int sum(ArrayList<Integer> numbers) {  
    int sum = 0;  
    for (Integer number : numbers) {  
        sum = sum + number;  
    }  
    return sum;  
}
```


