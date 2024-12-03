![](https://i.imgur.com/Vjeg0fD.png)

```Java
public class Cubes {  
    public static void main(String[] args){  
        Scanner scanner = new Scanner(System.in);  
  
        while(true){  
            String input = scanner.nextLine();  
            if(input.equals("end")){  
                break;  
            }  
  
            int numInput = Integer.parseInt(input);  
            System.out.println(numInput * numInput * numInput);  
        }  
    }  
}
```