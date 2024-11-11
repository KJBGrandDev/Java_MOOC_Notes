The ArrayList contains a bunch of useful methods. The method always operates on the list object that is connected to the method call — this connection is established with a dot. The example below illustrates that a program can contain multiple lists, which also holds true for other variables. Two separate lists are created below.

```Java
ArrayList<String> exercises1 = new ArrayList<>();
ArrayList<String> exercises2 = new ArrayList<>();

exercises1.add("Ada Lovelace");
exercises1.add("Hello World! (Ja Mualima!)");
exercises1.add("Six");

exercises2.add("Adding a positive number");
exercises2.add("Employee's pension insurance");

System.out.println("The size of list 1: " + exercises1.size());
System.out.println("The size of list 2: " + exercises2.size());

System.out.println("The first value of the first list " + exercises1.get(0));
System.out.println("The last value of the second list " + exercises2.get(exercises2.size() - 1));
```

```Java
The size of list 1: 3 
The size of list 2: 2 
The first value of the first list Ada Lovelace 
The last value of the second list Employee's pension insurance
```

Each list is its own separate entity, and the list methods always concern the list that was used to call the method. A summary of some list methods is provided below. It's assumed that the created list contains variables of type string.

- Adding to a list is done with the method `add` that receives the value to be added as a parameter.

```java
ArrayList<String> list = new ArrayList<>();
list.add("hello world!");
```

- The number of elements in a list can be discovered with the non-parameterized method `size`; it returns an integer.

```java
ArrayList<String> list = new ArrayList<>();
int size = list.size();
System.out.println(size);
```

- You can retrieve a value from a certain index with the method `get` that is given the index at which the value resides as a parameter.

```java
ArrayList<String> list = new ArrayList<>();
list.add("hello world!");
String string = list.get(0);
System.out.println(string);
```

- Removing elements from a list is done with the help of `remove`. It receives as a parameter either the value that is to be removed, or the index of the value to be removed.

```java
ArrayList<String> list = new ArrayList<>();
// remove the string "hello world!"
list.remove("hello world!");
 // remove the value at index 3
list.remove(3);
```

- Checking for the existence of a value is done with the method `contains`. It's provided the value being searched for as a parameter, and it returns a boolean value.

```java
ArrayList<String> list = new ArrayList<>();
boolean found = list.contains("hello world!");
```