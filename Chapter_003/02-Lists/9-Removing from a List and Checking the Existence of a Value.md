The list's **remove** method removes the value that is located at the index that's given as the parameter. The parameter is an integer.

```Java
ArrayList<String> list = new ArrayList<>();

list.add("First");
list.add("Second");
list.add("Third");

list.remove(1);

System.out.println("Index 0 so the first value: " + list.get(0));
System.out.println("Index 1 so the second value: " + list.get(1));
```

```Java
Index 0 so the first value: First 
Index 1 so the second value: Third
```

If the parameter given to `remove` is the same type as the values in the list, but not an integer, (integers are used to remove from a given index), it can be used to remove a value directly from the list.

```Java
ArrayList<String> list = new ArrayList<>();

list.add("First");
list.add("Second");
list.add("Third");

list.remove("First");

System.out.println("Index 0 so the first value: " + list.get(0));
System.out.println("Index 1 so the second value: " + list.get(1));
```

```Java
Index 0 so the first value: Second 
Index 1 so the second value: Third
```

If the list contains integers, you cannot remove a number value by giving an `int` type parameter to the remove method. This would remove the number from the index that the parameter indicates, instead of an element on the list that has the same value as the parameter. To remove an integer type value you can convert the parameter to Integer type; this is achieved by the `valueOf` method of the Integer class.

```Java
ArrayList<Integer> list = new ArrayList<>();

list.add(15);
list.add(18);
list.add(21);
list.add(24);

list.remove(2);
list.remove(Integer.valueOf(15));

System.out.println("Int 0 so the first value: " + list.get(0));
System.out.println("Int 1 so the second value: " + list.get(1));
```

```Java
Index 0 so the first value: 18 
Index 1 so the second value: 24
```

The list method **contains** can be used to check the existence of a value in the list. The method receives the value to be searched as its parameter, and it returns a boolean type value (`true` or `false`) that indicates whether or not that value is stored in the list.

```Java
ArrayList<String> list = new ArrayList<>();

list.add("First");
list.add("Second");
list.add("Third");

System.out.println("Is the first found? " + list.contains("First"));

boolean found = list.contains("Second");
if(found){
	System.out.println("Second was found");
}

//or more simply
if(list.contains("Second")){
	System.out.println("Second can still be found");
}
```

```Java
Is the first found? true 
Second was found 
Second can still be found
```

![[Pasted image 20241024160305.png]]

```Java
public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        ArrayList<String> list = new ArrayList<>();
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("")) {
                break;
            }

            list.add(input);
        }
        //my solution
        
        System.out.println("Search for? ");
        String secondInput = scanner.nextLine();
        if(list.contains(secondInput)){
            System.out.println(secondInput + " was found!");
        } else {
            System.out.println(secondInput + " was not found!");
        }
    }
```

```Java
//recommended solution

System.out.print("Search for? ");  
String name = scanner.nextLine();  
if (list.contains(name)) {  
    System.out.println(name + " was found!");  
} else {  
    System.out.println(name + " was not found!");
```