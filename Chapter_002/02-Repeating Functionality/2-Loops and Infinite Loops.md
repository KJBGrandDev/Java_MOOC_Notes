A loop consists of an expression that determines whether or not the code within the loop should be repeated, along with a block containing the source code to be repeated. A loop takes the following form.

```java
while (_expression_) {
    // The content of the block wrapped in curly brackets
    // The block can have an unlimited amount of content
}
```

We'll use the value `true` as the loop's expression for now. This way, the loop's execution is always continued when the program arrives at the point that decides whether it should be repeated or not. This happens when the execution of the program first arrives at the loop expression for the first time, and also when it reaches the end of the loop's block.

The loop execution proceeds line-by-line. The following program outputs _I can program_ an infinite number of times.

```java
while (true) {
    System.out.println("I can program!");
}
```

A program that runs infinitely does not end on its own. In NetBeans, it can be shut down by clicking the red button located on the left side of the output window.