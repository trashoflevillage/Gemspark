# If Statements
If Statements are a way to make code only read under specific conditions. There are many types of If Statements that are derived from DiamondFire. Gemspark refers to them as 'Definitions', as they define how the If statement functions.

An If Statement is defined as
```if <definition> (conditions) {code}```
Additionally, if you append an ```!``` to the beginning of the definition it will inverse the statement to check if the condition is not true.

# Value Equals
The 'Value Equals' definition checks if the first [value](Values.md) provided is exactly equal to any of the subsequent [values]](Values.md).
The Value Equals keyword(s) are
``eq``, ``equals``, ``val``, ``==``
The parameters for the Value Equals if statement are as follows;
``( Any check, Any compareTo.. )``

Example usage:
``if == (x, 1, 5) {code} // The code will only run if 'x' is equal to 1 or 5.``


# Greater Than
The 'Greater Than' definition checks if the first [value](Values.md) provided is greater than any of the subsequent [values](Values.md).
The Greater Than keyword(s) are
``great``, ``>``
The parameters for the Greater Than if statement are as follows;
``( Number check, Number compareTo.. )``

Example usage:
``if > (x, 1, 5) {code} // The code will only run if 'x' is greater than 1 or 5.``


# Less Than
The 'Less Than' definition checks if the first [value](Values.md) provided is less than any of the subsequent [values](Values.md).
The Less Than keyword(s) are
``less``, ``<``
The parameters for the Less Than if statement are as follows;
``( Number check, Number compareTo.. )``

Example usage:
``if < (x, 1, 5) {code} // The code will only run if 'x' is less than 1 or 5.``


# Greater Than/Equal To
The 'Greater Than/Equal To' definition checks if the first [value](Values.md) provided is greater than any of the subsequent [values](Values.md) or equal to any of the subsequent [values](Values.md).
The Greater Than/Equal To keyword(s) are
``greatEq``, ``>=``
The parameters for the Greater Than/Equal To if statement are as follows;
``( Number check, Number compareTo.. )``

Example usage:
``if >= (x, 1, 5) {code} // The code will only run if 'x' is greater than 1 or 5 or equal to 1 or 5.``


# Less Than/Equal To
The 'Less Than/Equal To' definition checks if the first [value](Values.md) provided is less than any of the subsequent [values](Values.md) or equal to any of the subsequent [values](Values.md).
The Less Than/Equal To keyword(s) are
``lessEq``, ``<=``
The parameters for the Less Than/Equal To if statement are as follows;
``( Number check, Number compareTo.. )``

Example usage:
``if <= (x, 1, 5) {code} // The code will only run if 'x' is less than 1 or 5 or equal to 1 or 5.``


# String Contains
The 'String Contains' definition checks if the first [value](Values.md) provided contains any of the subsequent Strings.
The String Contains keyword(s) are
``contains``, ``has``, ``stringHas``
The parameters for the String Contains if statement are as follows;
``( ^String check, String compareTo.. )``

Example usage:
``if has (x, "Hello World!", "Goodbye World!") {code} // The code will only run if 'x' contains "Hello World!" or "Goodbye World!"``

# String Ends With
The 'String Ends With' definition checks if the first [value](Values.md) provided ends with any of the subsequent Strings.
The String Ends With keyword(s) are
``endsWith``, ``last``
The parameters for the String Ends With if statement are as follows;
``( String check, String compareEnd.. )``

Example usage:
```
if endsWith (x, "!") {code} // The code will only run if 'x' ends with "!"
if endsWith (x, ":)") {code} // It works with more than just individual characters!
```


# String Starts With
The 'String Starts With' definition checks if the first [value](Values.md) provided ends with any of the subsequent Strings.
The String Starts With keyword(s) are
``startsWith``, ``first``
The parameters for the String Starts With if statement are as follows;
``( String check, String compareStart.. )``

Example usage:
```
if startsWith (x, "A") {code} // The code will only run if 'x' starts with "A"
if startsWith (x, "Apple") {code} // It works with more than just individual characters!
```


# RegEx Comparison
The 'RegEx' Comparison definition checks if the first [value](Values.md) matches any of the subsequent regEx strings.
The RegEx Comparison keyword(s) are
``regEx``
The parameters for the String Starts With if statement are as follows;
``( String check, String regExComparison.. )``

Example usage:
```
if startsWith ("Appl", "Appl+e") {code} // This will not run, because the RegEx isn't matched.
if startsWith ("Appleee", "Appl+e") {code} // This will run, because the RegEx is matched.
```


# Within Range
The 'Within Range' definition checks if the first [value](Values.md) provided is within the following two [values](Values.md). It will not check if the [values](Values.md) are equal.
The Within Range keyword(s) are
``within``
The parameters for the Within Range if statement are as follows;
``( Number check, Number rangeMin, Number rangeMax )``
``( Location check, Location rangeMin, Location rangeMax )``

Example usage:
```
if within (x, 5, 8) {code} // The code will only run if 'x' is within 5 and 8.
if within (5, 5, 8) {code} // This will not run.
if within (7, 5, 8) {code} // This will run.
```

```
a = newLoc(0, 0, 0);
b = newLoc(5, 50, 5);
if within (x, a, b) {code} // The code will only run if 'x' is within a and b.
```


# Near Location
The 'Near Location' definition checks if the first [value](Values.md) provided is within the provided radius of the provided comparing location(s).
The Near Location keyword(s) are
``near``
The parameters for the Near Location if statement are as follows;
``( Location compare1, Location(s) compare2, Number radius )``

Example usage:
```
a = newLoc(0, 0, 0);
b = newLoc(5, 75, 8);
c = newLoc(5.7, 75, 8.1);
if within (a, b, 3) {code} // The code will not run, because 'a' is not near enough to 'b'.
if withing (c, b, 3) {code} // However, 'c' is within 'b's radius of 3, so it does run!
```
# List Contains
The 'List Contains' definition checks if the list provided contains any of the subsequent [values](Values.md).
The List Contains keyword(s) are
``contains``, ``has``, ``listHas``
The parameters for the List Contains if statement are as follows;
``( ^List check, Any compareTo.. )``

Example usage:
``if has (x, 23, 81) {code} // The code will only run if 'x' contains 23 or 81.``

# List Value Equals
The 'List Value Equals' definition checks if a list's index has a specific [value](Values.md).
The List Value Equals keyword(s) are
``index``
The parameters for the List Value Equals if statement are as follows;
``( List check, Number index, Any compareTo )``

Example usage:
``if index (x, 5, "Hello!") {code} // The code will only run if 'x's 5th index is equal to "Hello!"``

# Dictionary Has Key
The 'Dictionary Has Key' definition checks if a dictionary has a specified key.
The Dictionary Has Key keyword(s) are
``contains``, ``has``, ``hasKey``, ``dictHas``
The parameters for the Dictionary Has Key if statement are as follows;
``( ^Dict check, String key )``

Example usage:
``if hasKey (x, "keyName") {code} // The code will only run if 'x' has a key with the name "keyName".``

# Dictionary Value Equals
The 'Dictionary Value Equals' definition checks if a dictionary's key is equal to the specified [value](Values.md).
The Dictionary Value Equals keyword(s) are
``keyEq``, ``keyIs``, ``dictVal``
The parameters for the Dictionary Value Equals if statement are as follows;
``( Dict check, String key, Any check2)``

Example usage:
```
if keyIs (x, "keyName", y) {code} // The code will only run if 'x' 
has a key with the name "keyName" and the value of 'y'.
```

# Item Has Tag
The 'Item Has Tag' definition allows users to detect if an Item has a tag or not. Additionally, there is an optional third parameter for also checking the [value](Values.md) of the tag.
The Item Has Tag keyword(s) are
``has``, ``hasTag``, ``itemHas``
The parameters for the Item Has Tag if statement are as follows;
``( ^Item check, String tagName, String tagValue*)``
``( ^Item check, String tagName, Number tagValue*)``
\* = Optional

Example Usage:
```
if hasTag (x, "tagname") {code} // This would run if the item had the specified tag, regardless of the value.
if hasTag (x, "tagname" "value") // This would run if the item had the specified tag along with the specified value.
```

# Value Is Type
The 'Value Is Type' definition compares the types of the two provided [values](Values.md).
The Value Is Type keyword(s) are
``type``
The parameters for the Value Is Type if statement are as follows;
``( Any compare, ^Any compare2 )``

Example Usage:
```
Wild checkValue = "Hello World!";
String checkValueB = "Goodbye World!";
if type (checkValue, checkValueB) {code} // This will work, since the first parameter allows Wild values.
if type (checkValueB, checkValue) {code} // This will not work, since the first parameter does 
not allow Wild values.
```

# Variable Exists
The 'Variable Exists' definition checks if the specified variable exists. Due to this functionality, the compiler will not throw an error if the variable being checked does not exist in the current context.
The Variable Exists keyword(s) are
``exists``
The parameters for the Variable Exists if statement are as follows;
``( Any check )``

Example Usage:
```
int x = 5;
if exists (x) {code} // This code will run because 'x' exists.
if exists (y) {code} // However, this code will not run because 'y' does not exist.
```
