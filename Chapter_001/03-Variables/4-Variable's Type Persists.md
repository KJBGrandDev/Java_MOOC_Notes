Once a variable's type has been declared, it can no longer be changed.

For example, a boolean value cannot be assigned of the integer type variable, nor an integer be assigned to a variable of the boolean type.
```Java
boolean integerAssignmentWillWork = false;
integerAssignmentWillWork = 42; //Does not work

int value = 10;
integerAssignmentWillWork = value; //Neither does this
```

However, exceptions do exist: an integer can be assigned to a variable of the "double" type, since Java knows how to convert an integer to a double during assignment.
```Java
double floatingPoint = 0.42;
floatingPoint = 1; //Works

int value = 10;
floatingPoint = value; //Also works
```

A floating-point value cannot, however be assigned to an integer variable. The reason for this is that those who develop the language aim to prevent developers from making errors that lead to a loss of information.
```Java
int value = 4.2; //Does not work

double floatingPoint = 0.42;
value = floatingPoint; //Neither does this
```