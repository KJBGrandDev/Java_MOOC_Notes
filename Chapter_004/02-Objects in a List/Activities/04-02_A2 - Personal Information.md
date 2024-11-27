![](https://i.imgur.com/b9hkSds.png)

```Java
public class PersonalInformationCollection {  
  
    public static void main(String[] args) {  
        // implement here your program that uses the PersonalInformation class  
        ArrayList<PersonalInformation> infoCollection = new ArrayList<>();  
        Scanner scanner = new Scanner(System.in);  
  
        while(true){  
            System.out.println("First name: ");  
            String firstName = scanner.nextLine();  
  
            if(firstName.isEmpty()){  
                break;  
            }  
  
            System.out.println("Last name: ");  
            String lastName = scanner.nextLine();  
  
            System.out.println("Identification Number: ");  
            String identificationNumber = scanner.nextLine();  
  
            infoCollection.add(new PersonalInformation(firstName, lastName, identificationNumber));  
        }  
  
        for(PersonalInformation output: infoCollection){  
            System.out.println(output.getFirstName() + " " + output.getLastName());  
        }  
    }  
}
```