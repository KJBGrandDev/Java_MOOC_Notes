A class specifies what the objects instantiated from it are like.

- The **object's variables (instance variables)** specify the internal state of the object
- The **object's methods** specify what the object does

We'll now familiarize ourselves with creating our own classes and defining the variable that belong to them.

A class is defined to represent some meaningful entity, where a "meaningful entity" often refers to a real-world object or concept. If a computer program had to process personal information, it would perhaps be meaningful to define a seperate class `Person` consisting of methods and attributes related to an individual.

Let's begin. We'll assume that we have a project template that has an empty main program:

```Java
public class main{
	public static void main(String[] args){
		
	}
}
```

![](https://i.imgur.com/bKZbecJ.png)

Let's create a class named `Person`. For this class, we create a separate file named `Person.java`. Our program now consists of two separate files since the main program is also in its own file. The `Person.java` file initially contains the class definition **public class Person** and the curly brackets that confine the contents of the class.

```Java
public class Person{

}
```

After creating a new file in NetBeans, the current state is as follows. In the image below, the class `Person` has been added to the SandboxExercise.

![](https://i.imgur.com/g7sPwPo.png)

You can also draw a class diagram to depict a class. We'll become familiar with its notations as we go along. An empty person-named class looks like this:

![](https://i.imgur.com/Knunnnt.png)

A class defines the attributes and behaviors of objects that are created from it. Let's decide that each person object has a name and an age. It's natural to represent the name as a string, and the age as an integer. We'll go ahead and add these to our blueprint:

```Java
public class Person {
 private String name;
 private int age;
}
```

We specify above that each object created from the `Person` class has a `name` and an `age`. Variables defined inside a class are called **instance variables**, or object fields or object attributes. Other names also seem to exist.

Instance variables are written on the lines following the class definition `public class Person {`. Each variable is preceded by the keyword private. 

The keyword **private** means that the variables are "hidden" inside the object. This is known as **encapsulation**.

In the class diagram, the variables associated with the class are defined as "variableName: variableType". The minus sign before the variable name indicates that the variable is encapsulated (it has the keyword private).

![](https://i.imgur.com/xxdqb06.png)

We have now defined a blueprint — a class — for the person object. Each new person object has the variables `name` and `age`, which are able to hold object-specific values. The "state" of a person consists of the values assigned to their name and age.
