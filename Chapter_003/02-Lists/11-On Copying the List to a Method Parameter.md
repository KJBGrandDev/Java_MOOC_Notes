Earlier we have used integers, floating point numbers, etc. as method parameters. When variables such as `int` are used as method parameters, the value of the variable is copied for the method's use. The same occurs in the case that the parameter is a list.

Lists, among practically all the variables that can store large amounts of information, are _reference-type variables_. This means that the value of the variable is a reference that points to the location that contains the information.

When a list (or any reference-type variable) is copied for a method's use, the method receives the value of the list variable, i.e., a _reference_. In such a case the **method receives a reference to the real value of a reference-type variable**, and the method is able to modify the value of the original reference type variable, such as a list. In practice, the list that the method receives as a parameter is the same list that is used in the program that calls the method.

Let's look at this briefly with the following method.

```Java
public static void removeFirst(ArrayList<Integer> numbers){
	if(numbers.size() == 0){
		return;
	}
	numbers.remove(0);
}
```

```Java
ArrayList<Integer> numbers = new ArrayList<>();
numbers.add(3);
numbers.add(2);
numbers.add(6);
numbers.add(-1);

System.out.println(numbers);

removeFirst(numbers);

System.out.println(numbers);

removeFirst(numbers);
removeFirst(numbers);
removeFirst(numbers);

System.out.println(numbers);
```

```Java
[3, 2, 6, -1] 
[2, 6, -1] 
[]
```

![[Pasted image 20241024193318.png]]

```Java
public static void main(String[] args) {
        // Try your method in here
        ArrayList<String> strings = new ArrayList<>();

        strings.add("First");
        strings.add("Second");
        strings.add("Third");

        System.out.println(strings);

        removeLast(strings);
        removeLast(strings);

        System.out.println(strings);
    }
    //my solution
    public static void removeLast(ArrayList<String> strings){
        if(strings.size() == 0){
            return;
        }
        int size = strings.size() - 1;
        strings.remove(size);
    }
```

```Java
//recommended solution
public static void removeLast(ArrayList<String> strings) {  
    if (strings.size() == 0) {  
        return;  
    }  
  
    strings.remove(strings.size() - 1);  
}
```

