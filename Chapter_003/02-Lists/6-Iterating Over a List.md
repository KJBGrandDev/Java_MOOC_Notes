We'll next be examining methods that can be used to go through the values on a list. Let's start with a simple example where we print a list containing four values.

```java
ArrayList<String> teachers = new ArrayList<>();

teachers.add("Simon");
teachers.add("Samuel");
teachers.add("Ann");
teachers.add("Anna");

System.out.println(teachers.get(0));
System.out.println(teachers.get(1));
System.out.println(teachers.get(2));
System.out.println(teachers.get(3));
```

```Java
Simon 
Samuel 
Ann 
Anna
```

The example is obviously clumsy. What if there were more values on the list? Or fewer? What if we didn't know the number of values on the list?

The number of values on a list is provided by the list's **size** method which returns the number of elements the list contains. The number is an integer (`int`), and it can be used as a part of an expression or stored in an integer variable for later use.

```Java
ArrayList<String> list = new ArrayList<>();
System.out.println("Number of values on the list: " + list.size());

list.add("First");
System.out.println("Number of values on the list: " + list.size());

int values = list.size();
System.out.println("Number of values on the lsit: " + list.size());
```

```Java
Number of values on the list: 0 
Number of values on the list: 1 
Number of values on the list: 1
```

![[Pasted image 20241007001106.png]]
