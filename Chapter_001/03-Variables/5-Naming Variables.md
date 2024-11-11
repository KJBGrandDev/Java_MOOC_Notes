Naming variables is a fundamental aspect of describing a program. Let's look at two examples:
```Java
double a = 3.14;
double b = 22.0;
double c = a * b * b;

System.out.println(c); //1519.76
```

```Java
double pi = 3.14;
double radius = 22.0;
double surfaceArea = pi * radius * radius;

System.out.println(surfaceArea); //1519.76
```

Both of the preceding examples function the same way and output the same result. One of them is, however, much more understandable.

The objective here is to compute the surfaces area of a circle. The value of pi is defined in the first row, the circle's radius in the second, and the surface area calculated in the third.

## Variables Express the Program and the Problem to be Solved
- Programming is a problem-solving tool. The aim is to create solutions for any given problem, such as the automation of control in cars. As a problem is approached, the developer decides on the terms used to describe the problem domain. The terminology that is chosen, such as variable names, will serve to describe the problem for anyone who is to work with it in the future.
- As you're wording the problem that you're solving, think about the concepts related to that problem and appropriate terms that could be used to describe them. If you find it hard to come up with relevant names, think of the ones that definitely do not describe it. After this, settle on some terminology that you're going to use - the good thing is that you can usually improve it later on.

Variable naming is limited by certain constraints.

Variable names cannot contain certain special symbols, such as an exclamation marks (!). Spaces are also not allowed, since they're used to separate parts of commands. Instead of spaces, the convention in java is to use a style known as "camelCase". Note! The first letter of a variable name is always lower-cased:
```Java
int camelCaseVariable = 7;
```

Numbers can be used within a variable name as long as the name does not begin with a number. Also, a name cannot consists of numbers only.
```Java
int 7variable = 4; //Not allowed
int variable7 = 4; //Allowed, but is not a descripting variable name
```

A variable's name cannot already be in use. These names include, for instance, variables previously defined in the program and commands provided by Java, such as "System.out.print" and "System.out.println"
```Java
int System.out.print = 4; //Not allowed
int System.out.println = 4; //Not allowed
```

```Java
int camelCase = 2;
int camelCase = 5; //Not allowed -- variable is already in used!
```

Letters containing diacritics (e.g. the letters ä and ö used in Finnish) should also not be used in variable names. You can replaces these letters with their non-diacritic equivalents. For example, you should convert ä -> a and ö -> o.

## Permissible Variable Names
- lastDayOfMonth = 20;
- firstYear = 1952;
- name = "Essi";

## Impermissible Variable Names
- last day of month = 20;
- 1day = 1952;
- beware! = 1910;