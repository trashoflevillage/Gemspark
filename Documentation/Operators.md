# Operator
**Note: The Operator documentation expects you to have a complete understanding of [functions](Functions.md)!**<br>
Operators function nearly identical to [functions](Functions.md), however they are declared and utilized differently.

A good example of an operator would be ``+``. 
```
Number x = 3 + 4; // This is an example of an operator in action!
```

## Declaration
To start the declaration of an operator, use the ``op`` keyword in the top layer of the program. Following this, you need to put the name of your operator. Right now your declaration should look like this:
```
op operatorName {

}
```
Now when you type your operator's name somewhere in the program, it will execute whatever code is inside of the operator's declaration.

## Parameters
To make this operator interact with adjacent values, inside of the declaration, on the side that you want the operator to interact with, add parentheses with a parameter inside of them.
```
op (Number num) operatorName {
	// This operator will interact with a number to the left of it.
}

op (Number num1) operator2 (Number num2) {
	// This operator will interact with a number on the left and right of it.
}
```
If an operator checks for a value and it is either the wrong type of value or no value is found, an error will be thrown.

## Return Values
Return Values work the same as they do in [functions](Functions.md), however the ``set`` keyword works slightly differently.
The ``set`` keyword works nearly identically to how it works in [functions](Functions.md), however the it will always change the *left* parameter. If there is no left parameter and you use the ``set`` keyword, an error will be thrown.

```
op (Number num) + (Number num2) -> Number {
	set Add(num, num2); // A recreation of the '+' functionality using the 'set' keyword.
}
```
