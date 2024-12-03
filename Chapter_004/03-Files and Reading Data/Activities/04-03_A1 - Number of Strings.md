![](https://i.imgur.com/gvG3C8l.png)
![](https://i.imgur.com/nurLBwC.png)

```Java
public class NumberOfStrings {  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in);  
  
        int i = 0;  
        while(true){  
            String input = scanner.nextLine();  
            if(input.equals("end")){  
                break;  
            }  
            i++;  
        }  
        System.out.println(i);  
    }  
}
```