# Variables
Variables allow you to store and modify [values](Values.md) in a complex way. Variables are *essential* to utilize Gemspark's full potential.

## Declaration & Re-assigning
Variables can store any type of [value](Values.md), however it must be specified what kind of [value](Values.md) they are storing when they are declared.

To declare a variable, you must type the [value type](Values.md) they are storing.

To re-assign a variable, it's the same as declaration, just without the type! Attempting to re-assign a variable that was never assigned in the first place will result in a compilation error.

Here is an example of variable declaration:
```
Number x = 72; // This will set the variable 'x' to 72.
x = 10; // Re-assign 'x' to 10.
x = "Hello!"; /* Since 'x' is of type Number, 
attempting to set it to something other than a Number will result in a compilation error.*/
Wild y = 72 // Wild variables can be set to any type.
y = "Hello!" // Therefor they can be reassigned to a new type, too.
```

To use a variable, you simply need to type the variable's name where you want to use it! For example;
```
String x = "Hello World!";
default.sendMessage(x); /* When the sendMessage function is called, 
it will utilize the value of 'x', which in this case is "Hello World!"*/
```
