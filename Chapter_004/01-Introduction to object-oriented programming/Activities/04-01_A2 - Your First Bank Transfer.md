![](https://i.imgur.com/9ixuvv0.png)

```Java
// My Solution -- YourFirstBankAccount.java
public static void main(String[] args) {
        // Do not touch the code in Account.java
        // write your program here
        Account matthewsAccount = new Account("Matthews account", 1000.00);
        Account myAccount = new Account("My account", 0.0);
        
        matthewsAccount.withdrawal(100);
        myAccount.deposit(100);
        System.out.println(matthewsAccount);
        System.out.println(myAccount);
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

    public double balance() {
        return this.balance;
    }

    @Override
    public String toString() {
        return this.owner + " balance: " + this.balance;
    }
}

```