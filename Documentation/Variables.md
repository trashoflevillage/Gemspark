# Variables
Variables are essentially a container for [values](Values.md).

## Declaration & Re-assigning
Variables can store any type of [value](Values.md), however it must be specified what kind of [value](Values.md) they are storing when they are declared.

To declare a variable, you must type the [value type](Values.md) they are storing. If you do not want to assign a static type to a variable, you can use `Dyn` instead to create a dynamic variable.

To re-assign a variable, it's the same as declaration, just without the type! Attempting to re-assign a variable that was never assigned in the first place will result in a compilation error.

Here is an example of variable declaration:
```
Number x = 72; // This will set the variable 'x' to 72.
x = 10; // Re-assign 'x' to 10.
x = "Hello!"; /* Since 'x' is of type Number, 
attempting to set it to something other than a Number will result in a compilation error.*/
Dyn y = 72 // Dyn variables can be set to any type of value.
y = "Hello!" // Therefor they can be reassigned to a new type, too.
```

To use a variable, you simply need to type the variable's name where you want to use it! For example;
```
String x = "Hello World!";
default.sendMessage(x); /* When the sendMessage function is called, 
it will utilize the value of 'x', which in this case is "Hello World!"*/
```
