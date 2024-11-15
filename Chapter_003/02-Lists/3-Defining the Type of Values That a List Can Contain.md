When defining the type of values that a list can include, the first letter of the element type has to be capitalized. A list that includes int-type variables has to be defined in the form `ArrayList<Integer>`; and a list that includes double-type variables is defined in the form `ArrayList<Double>`.

The reason for this has to do with how the ArrayList is implemented. Variables in Java can be divided into two categories: value type (primitive) and reference type (reference type) variables. **Value-type** variables such as `int` or `double` hold their actual values. **Reference-type** variables such as `ArrayList`, in contrast, contain a reference to the location that contains the value(s) relating to that variable.

Value-type variables can hold a very limited amount of information, whereas references can store a near limitless amount of it.

You'll find examples below of creating lists that contain different types of values.

```Java
ArrayList<Integer> list = new ArrayList<>();
list.add(1);
```

```Java
ArrayList<Double> list = new ArrayList<>();
list.add(4.2);
```

```Java
ArrayList<Boolean> list = new ArrayList<>();
list.add(true);
```

```Java
ArrayList<String> list = new ArrayList<>();
list.add("String is a reference-type variable");
```

Once a list has been created, ArrayList assumes that all the variables contained in it are reference types. Java automatically converts an `int` variable into `Integer` when one is added to a list, and the same occurs when a variable is retrieved from a list. The same conversion occurs for `double`-type variables, which are converted to `Double`. This means that even though a list is defined to contain `Integer`-type variables, variables of type `int` can also be added to it.

```Java
ArrayList<Integer> integers = new ArrayList<>();
int integer = 1;
integers.add(integer);

ArrayList<Double> doubles = new ArrayList<>();
double d = 4.2;
doubles.add(d);
```

We'll be returning to this theme since the categorization of variables into value and reference types affects our programs in other ways as well.