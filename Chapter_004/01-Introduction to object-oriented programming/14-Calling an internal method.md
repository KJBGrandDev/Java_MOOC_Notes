The object may also call its methods. For example, if we wanted the string representation returned by toString to also tell of a person's body mass index, the object's own `bodyMassIndex` method should be called in the `toString` method:

```java
public String toString() {
    return this.name + ", age " + this.age + " years, my body mass index is " + this.bodyMassIndex();
}
```

So, when an object calls an internal method, the name of the method and this prefix suffice. An alternative way is to call the object's own method in the form `bodyMassIndex()`, whereby no emphasis is placed on the fact that the object's own bodyMassIndex method is being called:

```java
public String toString() {
    return this.name + ", age " + this.age + " years, my body mass index is " + bodyMassIndex();
}
```