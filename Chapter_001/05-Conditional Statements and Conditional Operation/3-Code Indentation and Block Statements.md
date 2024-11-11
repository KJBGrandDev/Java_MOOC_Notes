A code block refers to a section enclosed by a pair of curly brackets. The source file containing the program includes the string `public class`, which is followed by the name of the program and the opening curly bracket of the block. The block ends in a closing curly bracket. In the picture below, the program block is highlighted.
![[Pasted image 20240831220910.png]]
The recurring snippet `public static void main(String[] args)` in the programs begins a block, and the source code within it is executed when the program is run — this snippet is, in fact, the starting point of all programs. We actually have two blocks in the example above, as can be seen from the image below.
![[Pasted image 20240831220959.png]]
Blocks define a program's structure and its bounds. A curly bracket must always have a matching pair: any code that's missing a closing (or opening) curly bracket is "erroneous".
- Erroneous = wrong; incorrect.

A conditional statement also marks the start of a new code block.

In addition to the defining program structure and functionality, block statements also have an effect on the readability of a program. Code living inside a block is indented. For example, any source code inside the block of a conditional statement is indented four spaces deeper than the `if` command that started the conditional statement. Four spaces can also be added by pressing the tab key (the key to the left of 'q'). When the block ends, i.e., when we encounter a `}` character, the indentation also ends. The `}` character is at the same level of indentation as the `if`-command that started the conditional statement.

The example below is incorrectly indented.

```Java
if (number > 10){
number = 9;
}
```

The example below is correctly indented.

```Java
if (number > 10){
	number = 9;
}
```