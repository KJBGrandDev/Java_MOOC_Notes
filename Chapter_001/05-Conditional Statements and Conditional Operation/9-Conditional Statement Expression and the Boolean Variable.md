The value that goes between the parentheses of the conditional statement should be of type boolean after the evaluation. `boolean` type variables are either _true_ or _false_.

```Java
boolean isItTrue = true;
System.out.println("The value of the boolean variable is " + isItTrue);

// The value of the boolean variable is true
```

The conditional statement can also be done as follows:

```java
boolean isItTrue = true;
if (isItTrue) //Truthy? {
    System.out.println("Pretty wild!");
}

// Pretty wild
```

Comparison operators can also be used outside of conditionals. In those cases, the boolean value resulting from the comparison is stored in a boolean variable for later use.

```Java
int first = 1;
int second = 3;
boolean isGreater = first > second;
```

In the example above, the boolean variable `isGreater` now contains the boolean value _false_. We can extend the previous example by adding a conditional statement to it.

```Java
int first = 1;
int second = 3;
boolean isLessThan = first < second;

if(isLessThan){
	System.out.println("1 is less than 3!");
}
```

![[Pasted image 20240831234103.png]]
The code in the image above has been executed to the point where the program's variables have been created and assigned values. The variable `isLessThan` has `true` as its value. Next in the execution is the comparison `if (isLessThan)` — the value for the variable `isLessThan` is found in its container, and the program finally prints:

```Java
1 is less than 3!
```