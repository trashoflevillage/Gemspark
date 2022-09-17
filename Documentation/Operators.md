# Operator
**Note: The Operator documentation expects you to have a complete understanding of [functions](Functions.md)!**<br>
Operators function nearly identical to [functions](Functions.md), however they are declared and utilized differently.

A good example of an operator would be ``+``. 
```
Number x = 3 + 4; // This is an example of an operator in action!
```

## Declaration
To start the declaration of an operator, use the ``op`` keyword in the top layer of the program. Following this, you need to put the name of your operator.
You also need to state a precedence alongside the operator's name. You can do this by surrounding a number with ``{}``.
A statement with multiple operators will execute the operators with the highest precedence first.
Parentheses interact with operators the same as they do in math.
Right now your declaration should look like this:
```
op operatorName{1} {

}
```
Now when you type your operator's name somewhere in the program, it will execute whatever code is inside of the operator's declaration.

## Parameters
To make this operator interact with adjacent values, inside of the declaration, on the side that you want the operator to interact with, add parentheses with a parameter inside of them.
```
op (Number num) operatorName{1} {
	// This operator will interact with a number to the left of it.
}

op (Number num1) operator2{1} (Number num2) {
	// This operator will interact with a number on the left and right of it.
}
```
If an operator checks for a value and it is either the wrong type of value or no value is found, an error will be thrown.

## Return Values
Return Values work the same as they do in [functions](Functions.md), however the ``set`` keyword works slightly differently.
The ``set`` keyword works nearly identically to how it works in [functions](Functions.md), however the it will always change the *left* parameter. If there is no left parameter and you use the ``set`` keyword, an error will be thrown.

```
op (Number num) +{1} (Number num2) -> Number {
	return Add(num, num2); // A recreation of the '+' functionality of other languages using the 'return' keyword.
}

op (Number num) +={1} (Number num2) -> Number {
	set Add(num, num2); // A recreation of the '+=' functionality of other languages using the 'set' keyword.
}
```
