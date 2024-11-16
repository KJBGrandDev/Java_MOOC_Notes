![](https://i.imgur.com/LjXiYXp.png)

```Java
// My Solution -- YourFirstAccount.java
public static void main(String[] args) {
        // Do not touch the code in Account.java
        // Write your program here
        Account artosAccount = new Account("Arto's account", 100.00);
        
        System.out.println("Initial state");
        System.out.println(artosAccount);
        
        artosAccount.deposit(20);
        System.out.println("End state");
        System.out.println(artosAccount);
    }
```

------------------------------------------------------------------------
#### Given Code
```Java
// Account.java
public class Account {

    private double balance;
    private String owner;

    public Account(String owner, double balance) {
        this.balance = balance;
        this.owner = owner;
    }

    public void deposit(double amount) {
        this.balance = this.balance + amount;
    }

    public void withdrawal(double amount) {
        this.balance = this.balance - amount;
    }

    public double saldo() {
        return this.balance;
    }

    @Override
    public String toString() {
        return this.owner + " balance: " + this.balance;
    }
```