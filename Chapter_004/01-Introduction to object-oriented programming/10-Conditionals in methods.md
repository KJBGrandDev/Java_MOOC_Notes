As we came to notice, methods can contain source code in the same way as other parts of our program. Methods can have conditionals or loops, and other methods can also be called from them.

Let's now write a method for the person that determines if the person is of legal age. The method returns a boolean - either `true` or `false`:

```Java
public class person {
	// ...

	public boolean isOfLegalAge(){
		if (this.age < 18){
			return false;
		}
		// if this.age > 18
		return true;
	}
	
	/*
     The method could have been written more succinctly in the following way:
     
    public boolean isOfLegalAge() {
        return this.age >= 18;
    }
    */
}
```

And let's test it out:

```Java
public static void main(String[] args){
	Person pekka = new Person("Pekka");
	Person antti = new Person("Antti");

	int i = 0;
	while(i < 30){
		pekka.growOlder();
		i = i + 1;
	}

	antti.growOlder();

	System.out.println("");

	if(antti.isOfLegalAge()){
		System.out.print("of legal age: ");
		antti.printPerson();
	} else {
		System.out.println("underage: ");
		antti.printPerson();
	}

	if (pekka.isOfLegalAge()) {
        System.out.print("of legal age: ");
        pekka.printPerson();
    } else {
        System.out.print("underage: ");
        pekka.printPerson();
    }
}
```

```Java
underage: Antti, age 1 years 
of legal age: Pekka, age 30 years
```

Let's fine-tune the solution a bit more. In its current form, a person can only be "printed" in a way that includes both the name and the age. Situations exist, however, where we may only want to know the name of an object. Let's write a separate method for this use case:

```Java
public class Person{
	// ...

	public String getName(){
		return this.name;
	}
}
```

The `getName` method returns the instance variable `name` to the caller. The name of this method is somewhat strange. It is the convention in Java to name a method that returns an instance variable exactly this way, i.e., `getVariableName`. **Such methods are often referred to as "getters".**

The class as a whole:

![](https://i.imgur.com/fHUPZj1.png)

Let's mould the main program to use the new "getter" method:

```Java
public static void main(String[] args){
	Person pekka = new Person("Pekka");
	Person antti = new Person("Antti");

	int i = 0;
	while(i < 30){
		pekka.growOlder();
		i = i + 1;
	}

	antti.growOlder();

	System.out.println("");

	if(antti.isOfLegalAge()){
		System.out.println(antti.getName() + " is of legal age");
	} else {
		System.out.println(antti.getName() + " is underage");
	}

	if (pekka.isOfLegalAge()) {
        System.out.println(pekka.getName() + " is of legal age");
    } else {
        System.out.println(pekka.getName() + " is underage ");
    }
}
```

The print output is starting to turn out quit neat:

```Java
Antti is underage 
Pekka is of legal age
```

