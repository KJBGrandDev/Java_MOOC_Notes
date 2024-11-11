If you don't need to keep track of the index as you're going through a list's values, you can make use of the **for-each** loop. It differs from the previous loops in that it has no separate condition for repeating or incrementing.
```Java
ArrayList<String> list = new ArrayList<>();

teachers.add("Simon");
teachers.add("Samuel");
teachers.add("Ann");
teachers.add("Anna");

for(String teacher: teachers){
	System.out.println(teacher);
}
```

In practical terms, the for-each loop described above hides some parts of the for-loop we practiced earlier. The for-each loop would look like this if implemented as a for-loop:
```Java
ArrayList<String> list = new ArrayList<>();

teachers.add("Simon");
teachers.add("Samuel");
teachers.add("Ann");
teachers.add("Anna");
for(int i = 0; i < teachers.size(); i++){
	String teacher = teachers.get(i);
	//contents of the for each loop
	System.out.println(teacher);
}
```

In practice, the for-each loop examines the values of the list in order one at a time. The expression is defined in the following format: `for (TypeOfVariable nameOfVariable: nameOfList)`, where `TypeOfVariable` is the list's element type, and `nameOfVariable` is the variable that is used to store each value in the list as we go through it.

![[Pasted image 20241022225249.png]]
```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    ArrayList<Integer> list = new ArrayList<>();  
    while (true) {  
        int input = Integer.valueOf(scanner.nextLine());  
        if (input == -1) {  
            break;  
        }  
  
        list.add(input);  
    }  
  
    System.out.println("");  
  
    //my code 
    int total = 0;  
    for(Integer sum: list){  
        total += sum;  
    }  
    System.out.println("Sum: " + total);  
}
```

```Java
// recommended code
int sum = 0;  
int index = 0;  
while (index < list.size()) {  
    sum += list.get(index);  
    index++;  
}  
System.out.println("Sum: " + sum);
```

![[Pasted image 20241022231038.png]]
```Java
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    // implement here a program, that first reads user input  
    // adding them on a list until user gives -1.    // Then it computes the average of the numbers on the list    // and prints it.ArrayList<Integer> list = new ArrayList<>();  
  
while(true){  
    int num = Integer.valueOf(scanner.nextLine());  
    if(num == -1){  
        break;  
    }  
    list.add(num);  
}  
int sum = 0;  
for(int total: list){  
    sum = sum + total;  
}  
double average = (double) sum / list.size();  
System.out.println("Average: " + average);  
}
```

```Java
// recommended code
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    ArrayList<Integer> list = new ArrayList<>();  
    while (true) {  
        int input = Integer.valueOf(scanner.nextLine());  
        if (input == -1) {  
            break;  
        }  
  
        list.add(input);  
    }  
  
    System.out.println("");  
  
    int sum = 0;  
    int index = 0;  
    while (index < list.size()) {  
        sum += list.get(index);  
        index++;  
    }  
  
    System.out.println("Average: " + (1.0 * sum / list.size()));  
}
```