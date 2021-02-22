# Rolls

<<<<<<< HEAD
Unfortunately, the roll property currently has no functionality. However, we can learn it's functionality from comments in the DiceCloud code as well as the field names. The same is true of [saving throws](savingthrow.md).
=======
A roll component allows you to save a dice roll temporarily, allowing for the dice to have its value not change between components of an action that rely on the same roll.
>>>>>>> origin/content-that-hasnt-gone-live

## Components

### Name

The name of the property.

### Variable Name

The variable used to access the result of the roll from other properties. This accepts both uppercase and lowercase Latin characters, numbers and underscores but not any other characters.

### Roll

A calculation for the dice that are to be rolled, which will likely include dice rolls in the calculation.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

<<<<<<< HEAD
Note that all values listed her can only be accessed using the `#roll.<valueName>` syntax from a child of the property.

=======
>>>>>>> origin/content-that-hasnt-gone-live
### name

The name of the roll.

<<<<<<< HEAD
### rollResult

The parsed value in the roll field, if dice rolls are included then all non-roll components are parsed.
=======
### variableName\*

The variable name used to access the roll's results.

### roll

The string entered into the roll field, unparsed.

### rollResult

The parsed result of the roll. If dice rolls are part of the calculation, this will return the result of the dice from the most recent time it was rolled.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

>>>>>>> origin/content-that-hasnt-gone-live
