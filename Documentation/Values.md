# Values
Values are pieces of data that your plot can utilize. There are many different types of values, and they all vary the data they store. Each value has a different method of declaration. Additionally, the Plot and Selections store values that can be utilized by the program.

[Strings](#Strings) <br>
[Numbers](#Numbers) <br>
[Locations](#Locations) <br>
[Vectors](#Vectors) <br>
[Wilds](#Wilds) <br>
[Lists](#Lists) <br>


## Strings
A ``String`` is a type of value that stores a list of characters. Strings are often used for the displaying of messages to players. To define a String, surround the characters you want included in the String by ``"``'s.
``"Hello World!"``
Additionally, Strings allow for the use of [escape sequences](https://en.wikipedia.org/wiki/Escape_sequences_in_C).


## Numbers
A ``Number`` encompasses any real numbers that the program utilizes. 
You can define a Number by using numeric characters.
``1``
``-9``
``30.53``

## Locations
A ``Location`` can store a list of five Numbers. These numbers represent an in-game coordinate. Locations allow for the easy modification of the game's world.
You can define a Location by using the ``createLoc()`` [function](Functions.md).
``createLoc(5, 50, 5);``
``createLoc(5, 75, 8, 5, 8);``
``createLoc(20, 25, 15, 80);``

## Vectors
A ``Vector`` can store a list of four Numbers. The first three numbers represent the direction the Vector is facing, with the fourth number being the length of the Vector. Vectors are typically utilized for representing velocity.
You can define a Vector by using the ``createVec()`` [function](Functions.md).
``createVec(1, 1, 1, 5);``
``createVec(-2, 1, 6);``

## Wilds
``Wild`` values represent *every type of value.* A Wild value can be anything from a String to a Dictionary. The existence of these values is primarily for the sake of easily being able to translate DiamondFire code into Gemspark code.

## Lists
``List``s are what the name implies, they store a list of values. However, Lists can only store one type of value.
You can define a List by using the ``createList()`` [function](Functions.md).
