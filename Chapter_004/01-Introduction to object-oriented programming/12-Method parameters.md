Let's continue with the `Person` class once more. We've decided that we want to calculate people's body mass indexes. To do this, we write methods for the person to set both the height and the weight, and also a method to calculate the body mass index. The new and changed parts of the Person object are as follows:

```Java
public class Person{
	private String name;
	private int age;
	private int weight;
	private int height;

	public Person(String initialName){
		this.age = 0;
		this.weight = 0;
		this.height = 0;
		this.name = initialName;	
	}

	public void setHeight(int newHeight){
		this.height = newHeight
	}

	public void setWeight(int newWeight){
		this.weight = newWeight;
	}

	public double bodyMassIndex(){
		double heightPerHundred = this.height/100.0;
		return this.weight / (heightPerHundred * heightPerHundred);
	}

	// ...
}
```

The instance variables `height` and `weight` were added to the person. Values for these can be set using the `setHeight` and `setWeight` methods. Java's standard naming convention is used once again, that is, if the method's only purpose is to set a value to an instance variable, then it's named as `setVariableName`. **Value-setting methods are often called "setters"**. The new methods are put to use in the following case:

```Java
public static void main(String[] args){
	Person matti = new Person("Matti");
	Person juhana = new Person("Juhana");

	matti.setHeight(180);
	matti.setWeight(86);

	juhana.setHeight(175);
	juhana.setWeight(64);

	System.out.println(matti.getName() + ", body mass index is " + matti.bodyMassIndex());
	System.out.println(juhana.getName() + ", body mass index is " + juhana.bodyMassIndex());
}
```

```Java
Matti, body mass index is 26.54320987654321 
Juhana, body mass index is 20.897959183673468
```
