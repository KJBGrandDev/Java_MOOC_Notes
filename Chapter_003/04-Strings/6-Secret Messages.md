In the exercises above, we actually implemented a very simple decrypting method for secret messages. One variant of these hidden messages consists of the first character of each line. For example, the secret message "program" is hidden in the (somewhat cryptic) text below.

```Java
Polymorphous computations elaborate. 
Real calculators honour. 
Older desktops deliver. 
Great mainframes link. 
Reversed devices install. 
Additional workstations modem. 
Many microcomputers letter.
```

Let's continue along the same theme! You can get a character at a specified index of a string with the `charAt` method.

```Java
String text = "Hello World";
char character = text.charAt(0);
System.out.println(character);
```

```Java
H
```

