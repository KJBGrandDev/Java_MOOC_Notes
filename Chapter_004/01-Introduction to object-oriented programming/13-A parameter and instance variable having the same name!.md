In the preceding example, the `setHeight` method sets the value of the parameter `newHeight` to the instance variable `height`:

```Java
public void setHeight(int newHeight){
	this.height = newHeight;
}
```

The parameter's name could also be the same as the instance variable's, so the following would also work:

```Java
public void setHeight(int height){
	this.height = height;
}
```

In this case, `height` in the method refers specifically to a parameter named _height_ and `this.height` to an instance variable of the same name. For example, the following example would not work as the code does not refer to the instance variable _height_ at all. What the code does in effect is set the `height` variable received as a parameter to the value it already contains:

```java
public void setHeight(int height) {
    // DON'T DO THIS!!!
    height = height;
}
```

```java
public void setHeight(int height) {
    // DO THIS INSTEAD!!!
    this.height = height;
}
```

