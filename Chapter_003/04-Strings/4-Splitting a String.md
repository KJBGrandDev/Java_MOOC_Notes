You can split a string to multiple pieces with the `split`-method of the String class. The method takes as a parameter a string denoting the place around which the string should be split. The `split` method returns an array of the resulting sub-parts. In the example below, the string has been split around a space.

```Java
String text = "first second third fourth";
String[] pieces = text.split(" ");
System.out.println(pieces[0]);
System.out.println(pieces[1]);
System.out.println(pieces[2]);
System.out.println(pieces[3]);

System.out.println();

for(int i = 0; i < pieces.length; i++){
	System.out.println(pieces[i]);
}
```

```Java
first 
second 
third 
fourth

first 
second 
third 
fourth
```

![[Pasted image 20241028235852.png]]

```Java
// My Solution
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    int index = 0;  
    while(true){  
        String input = scanner.nextLine();  
        if(input.equals("")){  
            break;  
        }  
  
        String[] dividedStrings = input.split(" ");  
        while(index < dividedStrings.length){  
            System.out.println(dividedStrings[index]);  
            index++;  
        }  
        index = 0;  
    }  
}
```

```Java
// Recommended Solution
public static void main(String[] args) {  
    Scanner scanner = new Scanner(System.in);  
  
    while (true) {  
        String input = scanner.nextLine();  
        if (input.equals("")) {  
            break;  
        }  
  
        String[] parts = input.split(" ");  
        for (String part : parts) {  
            System.out.println(part);  
        }  
    }  
  
}
```

![[Pasted image 20241109004343.png]]
![[Pasted image 20241109004353.png]]

```Java
// My Solution
public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);

        while(true){
            String input = scanner.nextLine();
            if(input.equals("")){
                break;
                }
            String[] pieces = input.split(" ");
            for(String piece: pieces){
                if(piece.contains("av")){
                    System.out.println(piece);
                }
            }
        }
    }
```