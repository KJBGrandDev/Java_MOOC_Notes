![](https://i.imgur.com/Z75hcm0.png)

![](https://i.imgur.com/YI5ROK9.png)
![](https://i.imgur.com/ADRDn4o.png)
![](https://i.imgur.com/Ij0G9xE.png)

![](https://i.imgur.com/8GwyCTK.png)
![](https://i.imgur.com/AdvPqE4.png)
![](https://i.imgur.com/BuOenfd.png)

![](https://i.imgur.com/svwL2X5.png)
![](https://i.imgur.com/4K1MCXd.png)

![](https://i.imgur.com/GrKKFnb.png)
![](https://i.imgur.com/8u0pG02.png)

![](https://i.imgur.com/IsiwmPi.png)
![](https://i.imgur.com/locBce2.png)

![](https://i.imgur.com/A7XsF9w.png)
![](https://i.imgur.com/7dFRfeR.png)
![](https://i.imgur.com/7t1smXM.png)

```Java

// MainProgram.java

public class MainProgram {  
    public static void main(String[] args){  
        PaymentCard paul = new PaymentCard(20);  
        PaymentCard matt = new PaymentCard(30);  
  
        paul.eatHeartily();  
        matt.eatAffordably();  
  
        System.out.println("Paul: " + paul);  
        System.out.println("Matt: " + matt);  
  
        paul.addMoney(20);  
  
        matt.eatHeartily();  
  
        System.out.println("Paul: " + paul);  
        System.out.println("Matt: " + matt);  
  
        paul.eatAffordably();  
        paul.eatAffordably();  
  
        matt.addMoney(50);  
  
        System.out.println("Paul: " + paul);  
        System.out.println("Matt: " + matt);  
    }  
}
```

```Java

// PaymentCard.java

public class PaymentCard {  
    private double balance;  
  
    public PaymentCard(double openingBalance){  
        this.balance = openingBalance;  
    }  
  
    public String toString(){  
        return "The card has a balance of " + this.balance + " euros";  
    }  
  
    public void eatAffordably(){  
        double eatAffordably = 2.6;  
        if(this.balance >= eatAffordably){  
            this.balance = this.balance - eatAffordably;  
        }  
    }  
  
    public void eatHeartily(){  
        double eatHeartily = 4.6;  
        if(this.balance >= eatHeartily){  
            this.balance = this.balance - eatHeartily;  
        }  
    }  
  
    public void addMoney(double amount){  
        if(amount > 0 && this.balance + amount < 150){  
            this.balance = this.balance + amount;  
        } else if (amount > 0 && this.balance + amount > 150){  
            this.balance = 150;  
        }  
    }  
}
```