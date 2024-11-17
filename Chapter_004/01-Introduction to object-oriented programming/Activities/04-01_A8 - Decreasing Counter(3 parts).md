![](https://i.imgur.com/mR46hIK.png)

![](https://i.imgur.com/IbSWSrv.png)

![](https://i.imgur.com/nFSnaYm.png)

![](https://i.imgur.com/NFSXzp6.png)

```Java
public void decrement() {  
    // write the method implementation here  
    // the aim is to decrement the value of the counter by one
    if(this.value > 0){  
        this.value = this.value - 1;  
    }  
}
```

![](https://i.imgur.com/MUfdu7Y.png)

```Java
public void reset() {  
    this.value = 0;  
}
```

------------------------------------------------------------------------
#### Entire Code

```Java
public class DecreasingCounter {  
  
    private int value;  // an object variable for storing the value of the counter  
  
    public DecreasingCounter(int initialValue) {  
        this.value = initialValue;  
    }  
  
    public void printValue() {  
        // Do not change this code!  
        System.out.println("value: " + this.value);  
    }  
  
    public void decrement() {  
        // write the method implementation here  
        // the aim is to decrement the value of the counter by one        
        if(this.value > 0){  
            this.value = this.value - 1;  
        }  
    }  
  
    public void reset() {  
        this.value = 0;  
    }  
    // the other methods go here  
}
```