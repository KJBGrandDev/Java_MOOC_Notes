In the next exercise you'll be asked for the length of the names. You can find out the length of a string with `length()`-method:

```Java
String word = "equisterian";
int length = word.length();
System.out.println("The length of the word " + word + " is " + length); 
```

```Java
The length of the word equisterian is 11
```

![](https://i.imgur.com/vPbFSiq.png)

```Java
// My Solution
public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);

        String longestName = "";
        int currentLongestNameSize = 0;

        int numberOfInputs = 0;
        double averageYear = 0;

        while(true){
            String input = scanner.nextLine();
            if(input.equals("")){
                break;
            }

            String[] inputArray = input.split(",");
            String name = inputArray[0];
            int nameSize = inputArray[0].length();
            int birthYear = Integer.valueOf(inputArray[1]);

            if(nameSize > currentLongestNameSize){
                currentLongestNameSize = nameSize;
                longestName = name;
            }

            averageYear += birthYear;
            numberOfInputs++;
        }
        System.out.println("Longest name: " + longestName);
        System.out.println("Average of the birth years: " + (1.0 * (averageYear / numberOfInputs)));
    }
```

```Java
// Preferred Solution

public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
 
        ArrayList<String> names = new ArrayList<>();
        ArrayList<Integer> birthYears = new ArrayList<>();
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("")) {
                break;
            }
 
            String[] parts = input.split(",");
            names.add(parts[0]);
            birthYears.add(Integer.valueOf(parts[1]));
        }
        
        String longest = names.get(0);
        for (String name : names) {
            if(name.length() > longest.length()) {
                longest = name;
            }
        }
        System.out.println("Longest name: " + longest);
        
        int sumOfBirthYears = 0;
        for (int year : birthYears) {
            sumOfBirthYears = sumOfBirthYears + year;
        }
        System.out.println("Average of the birth years: " + 1.0 * sumOfBirthYears / birthYears.size());
 
    }
```