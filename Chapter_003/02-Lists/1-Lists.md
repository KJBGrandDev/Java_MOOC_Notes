### Learning Objectives

- You are familiar with the list structure and know how to use a list in a program.

- You are familiar with the concept of an index, you can add values to a list, and you know how to retrieve information from a list's indices.

- You know how to iterate over a list with multiple different loop types.

- You know how to check if a value exists in a list, and also know how to remove values from a list.

- You are aware of the list being a reference-type variable, and become familiar with using lists as method parameters.

In programming, we often encounter situations where we want to handle many values. The only method we've used so far has been to define a separate variable for storing each value. This is impractical.

```java
String word1;
String word2;
String word3;
// ...
String word10;
```

The solution presented above is useless in effect — consider a situation in which there are thousands of words to store.

Programming languages offer tools to assist in storing a large quantity of values. We will next take a peek at perhaps the single most used tool in Java, the [ArrayList](https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html), which is used for storing many values that are of the same type.

ArrayList is a pre-made tool in Java that helps dealing with lists. It offers various methods, including ones for adding values to the list, removing values from it, and also for the retrieval of a value from a specific place in the list. The concrete implementations — i.e., how the list is actually programmed — has been abstracted behind the methods, so that a programmer making use of a list doesn't need to concern themselves with its inner workings.