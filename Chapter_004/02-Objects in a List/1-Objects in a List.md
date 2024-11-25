### Learning Objectives

- You can add objects to a list

- You can go through objects in a list

The type parameter used in creating a list defines the type of the variables that are added to the list. For instance, `ArrayList<String>` includes strings, `ArrayList<Integer>` integers, and `ArrayList<Double>` floating point numbers

In the example below we first add strings to a list, after which the strings in the list are printed one by one.

```Java
ArrayList<String> names = new ArrayList<>();

// String can first be stored in a variable
String name = "Betty Jennings";
// then add it to the list
names.add(name);

// Strings can also be directly added to the list:
names.add("Betty Synder");
names.add("Frances Spence");
names.add("Kay McNulty");
names.add("Marlyn Wescoff");
names.add("Ruth Lichterman");

// several different repeat statements can be
// used to go through the list elements

// 1. while loop
int index = 0;
while(index < names.size()){
	System.out.println(names.get(index));
	index = index + 1;
}

// 2. for loop with index
for(int i = 0; i < names.size(); i++){
	System.out.println(names.get(i));
}

// 3. for each loop(no index)
for(String name: names){
	System.out.println(name);
}
```

```Java
Betty Jennings 
Betty Snyder 
Frances Spence 
Kay McNulty Marlyn 
Wescoff Ruth 
Lichterman

// Still same with the top side but not indented due to note size constraint (tackled by me)
Betty Jennings Betty Snyder Frances Spence Kay McNulty Marlyn Wescoff Ruth Lichterman

Betty Jennings Betty Snyder Frances Spence Kay McNulty Marlyn Wescoff Ruth Lichterman
```