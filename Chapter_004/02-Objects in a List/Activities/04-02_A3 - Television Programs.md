![](https://i.imgur.com/7cYEYNF.png)

```Java

// Main.java

public class Main {  
  
    public static void main(String[] args) {  
        // implement here your program that uses the TelevisionProgram class  
  
        ArrayList<TelevisionProgram> programs = new ArrayList<>();  
        Scanner scanner = new Scanner(System.in);  
  
        while(true){  
            System.out.println("Name: ");  
            String nameInput = scanner.nextLine();  
  
            if(nameInput.isEmpty()){  
                break;  
            }  
            System.out.println("Duration: ");  
            int ageInput = Integer.parseInt(scanner.nextLine());  
  
            programs.add(new TelevisionProgram(nameInput, ageInput));  
        }  
  
        System.out.println("Program's maximum duration? ");  
        int durationInput = Integer.parseInt(scanner.nextLine());  
  
        for(TelevisionProgram program: programs){  
            if(program.getDuration() <= durationInput){  
                System.out.println(program);  
            }  
        }  
    }  
}
```

```Java

// TelevisionProgram.java

public class TelevisionProgram {  
  
    private String name;  
    private int duration;  
  
    public TelevisionProgram(String name, int duration) {  
        this.name = name;  
        this.duration = duration;  
    }  
  
    public boolean isAwesome() {  
        return this.name.contains("MasterChef");  
    }  
  
    public String getName() {  
        return name;  
    }  
  
    public int getDuration() {  
        return duration;  
    }  
  
    @Override  
    public String toString() {  
        return this.name + ", " + this.duration + " minutes";  
    }  
}
```