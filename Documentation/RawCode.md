# Raw Code
Raw Code is the very backbone of Gemspark, it's what everything runs off of. It is the key to your conventional Gemspark code translating over to DiamondFire block code.
To use Raw Code, you *must* understand DiamondFire's block code.
The following elements of Gemspark can be declared with Raw Code:
[Functions](#Functions)
[Events](#Events)
[Fields](#Fields)
[If Statements](#If_Statements)
[Values](#Values)

## Functions
Raw functions are not literally functions. Whenever you use a raw function, it is replaced with whatever blocks are inside of it upon compilation. For this reason, raw functions should NOT be used conventionally. They should only be used for one or two code blocks. To declare a raw function, you must use the ``rawfun`` keyword before the function's name, as shown here:
```
rawfun functionName() {
	// Code blocks go here. This will be explained shortly.
}
```
Of course, these functions can take inputs like any other function. The types still must be specified.
```
rawfun functionName(String a, String b) {
	// Code blocks go here. This will be explained shortly.
}
```
Inside of a raw function, you can declare *code blocks*. These code blocks are identical to DiamondFire's code blocks, just in text form. This allows Gemspark to easily compile down to DiamondFire code blocks, and allows for the ability to easily add new DiamondFire features to Gemspark. To define a code block inside of a raw function, you must use a pair of square brackets with the code block's type. 
```
rawfun functionName(String a) {
	[player_action]
}
```
The following is a list of the valid block types;
``player_action``, ``entity_action``, ``set_var``, ``control``

Following the type, in a pair of curly braces you must put the action being executed by the block type. This is the *exact* text that shows on the code block signs in DiamondFire.
```
rawfun functionName(String a) {
	[player_action]{SendMessage}
}
```
Following the action in a pair of parentheses, you must input the parameters being utilized for the raw code.
```
rawfun functionName(String a) {
	[player_action]{SendMessage}(a)
}
```
If the code block you are using has tags, and you do not want the default tag(s), then you must follow all of this up by angle brackets. Inside of the angle brackets, put the tag's name followed by a colon, ending with the selected option. Once again, these must be typed out *exactly* as they are in DiamondFire.
```
rawfun functionName(String a) {
	[player_action]{SendMessage}(a)<Alignment Mode: Centered>
}
```
And to top it all of, you must append a semicolon to mark the end of the code block.
```
rawfun functionName(String a) {
	[player_action](SendMessage)(a)<Alignment Mode: Centered>;
}
```
Raw functions can be called the same as any other function by just typing the function's name followed by the parameters.
```
OnJoin @ PlayerJoinEvent {
	functionName("Hello world!");
}

rawfun functionName(String a) {
	[player_action](SendMessage)(a)<Alignment Mode: Centered>;
	// When called, runs the Player Action 'Send Message' on the default target.
}
```
If you want to run the code on a target other than the default, then you must use the `on` keyword followed by the desired [selector](Selectors.md) after the rest of the code block, excluding the semicolon.
```
OnJoin @ PlayerJoinEvent {
	functionName("Hello world!");
}

rawfun functionName(String a) {
	[player_action](SendMessage)(a)<Alignment Mode: Centered> on AllPlayers;
	// When called, runs the Player Action 'Send Message' on every player.
}
```

As stated previously, raw functions should not be used as replacement for normal functions. If you understand the raw code because you are familiar with DiamondFire and are contemplating using it exclusively, *do not*. That is inefficient practice, primarily because they are not viewed as real functions.

## Events
Using Raw Code, you can add events from DiamondFire that may not be currently supported by Gemspark. Whether it be because it was overlooked, deemed unnecessary, or a new event in DiamondFire that is not yet supported.
To create an event, use the ``rawev`` keyword, followed by the event's name as shown here:
```
rawev EventName
```
Following this, inside of square brackets you need to specify the event type.
```
rawev EventName[player]
```
The following is a list of the valid event types;
``player``, ``entity``

Following the event type, surrounded by curly braces you must specify the *exact* text that is on the event block's sign in DiamondFire for the event you are wanting to reference.
```
rawev EventName[player]{JoinEvent}
```
Now follow all of this up by a semicolon, and that's it! Now you can subscribe [processes](Processes.md) to your event!
```
rawev EventName[player]{Join};

pro ProcessName @ EventName {
	// This code runs whenever 'EventName' is triggered!
}
```

## Fields

## If Statements

## Values