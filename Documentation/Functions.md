# Functions
Functions are blocks of code that can be called by the program. Each function has a different name. A function can be defined with the ``fun`` keyword followed by the function's name and parameters. Functions must be declared in the top layer of the program.
``` 
fun functionName() {code}
```
To call a function, all you have to do is type the function name followed by parentheses.
```
functionName();
```

## Parameters
Functions can allow users to specify parameters for their functions. To specify that a function requires a parameter, inside of the function's parentheses you need to specify the [type](Values.md) of the parameter and the name of the parameter. If you want multiple parameters, you can separate them with commas.
```
fun functionName(String parameter1, Number parameter2) {code}
```
To use the parameters when calling the function, you simply need to put your input inside of the function call's parentheses.
```
functionName("Hello!", 1);
```
Whenever a function with parameters is called, the parameters act as local variables inside of the function.
For example;
```
fun sendAll(String message) {
	allPlayers.sendMessage(message);
}

sendAll("Hello World!"); /* Since we're calling the SendAll function with the parameter "Hello World!",
the message variable will be set to "Hello World!" inside of the function.*/
```

Additionally, if you want a function parameter to reject Wild [variables](Variables.md), then you can append a ``^`` to the beginning of the parameter's type, as seen here:
```
fun functionName(^String message) {
	// This function will allow Strings, as long as they aren't coming from a Wild variable
}
```

If you would like your function to run directly off of a value, then you can allow for that, too! To allow for this functionality, you can append an `&` before the function's name. This will result the first parameter not being specified in the parentheses of the function call, but rather the function call needs to be placed after the [value](Values.md) that the function is utilizing.
```
fun &sendAll(String message) {
	allPlayers.sendMessage(message);
}

sendAll("Hello World!"); /* This will *not* work, because the string is no longer an input, but rather the function runs off of the String.*/
String x = "Hello World!";
x.sendAll(); // However, this will run because the function is running off of the String.
```

## Return Types
Normally, you can type ``return;`` inside of a function to escape the function. However, functions can allow for return types, assuming the function specifies a return type.
To specify a return type for a function, you need to append ``-> Type`` to the end of the function's declaration.
```
fun FunctionName(Number num) -> Number {
	return num; /* If a function specifies a return type, it must have a return statement. This return
	statement must return the return type, and not another type.
}
```

When a function returns a value, the function call is seen as the return value by the code executing it.
For example;
```
fun Double(Number num) -> Number {
	return multiply(num, 2); // Return the input multiplied by 2.
}

Number x = 1 + Double(5); /* After the function call, this line of code is seen as
Number x = 1 + 10; because the 'Double' function returns 10.*/
```

Also, if the function runs on a value, you can use the ``set`` keyword. This keyword sets the value that the function is running on instead of the basic return functionality.
