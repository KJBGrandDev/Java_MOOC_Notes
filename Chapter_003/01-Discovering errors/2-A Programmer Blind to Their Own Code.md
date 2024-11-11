A programmer often becomes blind to their code.

There's something else that also happens in the video that may go unnoticed at first. This effect is known as **perceptual blindness**, and is explained by the fact that as we focus on a specific task, our brains tend to filter out information that is irrelevant to that task. However, we don't always know what information is, in fact, essential and what is not - an example of this being when we study. Concentrating on a specific part of a study exercise can lead to relevant information being filtered out.

Fortunately, applying oneself to a given task lessens the occurrence of perceptual blindness. In other words, practice develops one's ability to distinguish between relevant and irrelevant information.

One way in which perceptual blindness manifests itself in programming practice is when concentrating on a specific part of a program draws attention away from seemingly correct, yet erroneous parts. **For instance, while inspecting the correctness of a program's output, a programmer may fixate on the print statements, and mistakenly neglect some aspects of the logic.**

----------------------------------------------------------------------

Likewise, a programmer may focus on the most complicated aspect of a program featuring a loop, when in fact the error lies somewhere else completely. An example of this is the program below, which is used to calculate the average of user-inputted values. It contains an error, and when searching for it, the loop is typically the first target of focus.

```Java
Scanner scanner = new Scanner(System.in);
int values = 0;
int sum = 0;

while(true){
	System.out.println("Provide a value, a negative value ends the program");
	int value = Integer.valueOf(scanner.nextLine());
	if(value < 0){
		break;
	}
	values = values + 1;
	sum = sum + value;
}
if(sum == 0){
	System.out.println("The average of the values could not be calculated.");
} else {
	System.out.println("Average of values: " + (1.0 * sum / values));
}
```

Perceptual blindness is something that one cannot be eliminated completely. However, there are ways by which a programmer can lessen its effect - the first one being taking breaks, which requires that work is begun early. Code comments, proper naming of things, and "debugging" prints are additional examples of things that are also helpful.