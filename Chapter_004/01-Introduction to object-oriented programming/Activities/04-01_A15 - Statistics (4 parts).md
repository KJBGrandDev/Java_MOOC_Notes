![](https://i.imgur.com/hVcK6yd.png)
![](https://i.imgur.com/az4gOBx.png)
![](https://i.imgur.com/c5nmXC9.png)
![](https://i.imgur.com/dZqNOhD.png)
![](https://i.imgur.com/wFlRMgf.png)
![](https://i.imgur.com/POHfT0i.png)
![](https://i.imgur.com/uxtKdn1.png)

```Java

// MainProgram.java
import java.util.Scanner;
public class MainProgram {  
  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in);  
        // you can write test code here  
        // however, remove all unnecessary code when doing the final parts of the exercise  
        // In order for the tests to work, the objects must be created in the        // correct order in the main program. First the object that tracks the total        // sum, secondly the object that tracks the sum of even numbers,        // and lastly the one that tracks the sum of odd numbers!        Statistics statistics = new Statistics();  
        Statistics even = new Statistics();  
        Statistics odd = new Statistics();  
  
        System.out.println("Enter numbers:");  
        while (true) {  
            int input = Integer.parseInt(scanner.nextLine());  
            if(input == -1){  
                System.out.println("Sum: " + statistics.sum());  
                System.out.println("Sum of even numbers: " + even.sum());  
                System.out.println("Sum of odd numbers: " + odd.sum());  
                break;  
            }  
            if(input % 2 == 0){  
                even.addNumber(input);  
            }  
            if(input % 2 != 0){  
                odd.addNumber(input);  
            }  
            statistics.addNumber(input);  
        }  
    }  
}
```

```Java

// Statistics.java

public class Statistics {
    private int count;
    private int sum;

    public Statistics(){
        this.count = 0;
        this.sum = 0;
    }
    public void addNumber(int number){
        this.count = this.count + 1;
        this.sum = this.sum + number;
    }

    public int getCount(){
        return this.count;
    }

    public int sum(){
        return this.sum;
    }

    public double average(){
        if(this.count == 0){
            return 0;
        }
        return (double)this.sum/this.count;
    }
}
```