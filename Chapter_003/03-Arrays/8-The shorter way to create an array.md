Just like for Strings, there's also a shortcut to create an array. Here we create an array to hold 3 integers, and initiate it with values 100, 1 and 42 in it:

```Java
int[] numbers = {100, 1, 42};
```

So apart from calling for `new`, we can also initialize an array with a block, that contains comma-separated values to be assigned in the array. This works for all the types: below we initialize an array of strings, then an array of floating-point numbers. Finally the values are printed.

```Java
String[] arrayOfStrings = {"Matti L.", "Matti P.", "Matti V."};
double[] arrayOfFloatingPoints = {1.20, 3.14, 100.0, 0.6666666667};

for(int i = 0; i < arrayOfStrings.length; i++){
	System.out.println(arrayOfStrings[i] + " " + arrayOfFloatingPoints[i]);
}
```

```Java
Matti L. 1.20 
Matti P. 3.14 
Matti V. 100.0
```

When you initialize an array with a block, the length of the array is precisely the number of the values specified in the block. The values of the block are assigned to the array in the order, eg. the first value is assigned to index 0, the second value to index 1 etc.

```java
// index           0   1    2    3   4   5     6     7
int[] numbers = {100,  1,  42,  23,  1,  1, 3200, 3201};

// prints the number at index 0, i.e. number 100
System.out.println(numbers[0]);
// prints the number at index 2, i.e. number 42
System.out.println(numbers[2]);
```

Just like in ArrayLists, you can't access an index outside of the array. You can try out the following example on your own computer, for example in the sandbox.

```java
String[] arrayOfStrings = {"Matti L.", "Matti P.", "Matti V."};
double[] arrayOfFloatingpoints = {1.20, 3.14, 100.0, 0.6666666667};

for (int i = 0; i < arrayOfFloatingpoints.length; i++) {
    System.out.println(arrayOfStrings[i] + " " +  arrayOfFloatingpoints[i]);
}
```
