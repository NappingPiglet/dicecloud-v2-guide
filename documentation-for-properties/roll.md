# Rolls

A roll is used to store the result of a dice roll even after the character sheet recomputes.

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

### name

The name of the roll.

### variableName\*

The variable name used to access the roll's results.

### roll

The string entered into the roll field, unparsed.

### rollResult

The parsed result of the roll. If dice rolls are part of the calculation, this will return the result of the dice from the most recent time it was rolled.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

