# Saving Throws

Unfortunately, the saving throw property currently has no functionality. However, we can learn it's functionality from comments in the DiceCloud code as well as the field names. The same is true of [rolls](roll.md).

The saving throw component is used to automate rolling some quantity of dice in response to an action. The intended use of this seems to be activating abilities in response to certain dice rolls, at least from the comments.

> \* \# Rolls are resolved in one of two ways:  
> Saving throws:  
> \* The target number is computed in the action taker's context  
> \* The roll is computed in the target's context  
> \* If the roll fails to meet or exceed the target number, the adjustments and  
> \* child rolls are applied

## Components

### Name

The name of the saving throw.

### DC

The minimum roll needed to avoid suffering negative effects most likely. Accepts numbers and calculations

### Save

Which saving throw type skill this will target.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the saving throw.

### dc\*

The DC of the saving throw, unparsed.

### stat\*

The variable name of the skill the saving throw targets.

### dcResult\*

The DC of the saving throw, parsed. If dice rolls are included, then all non-dice rolls are parsed.

{% hint style="warning" %} Values marked by a \* can only be accessed using an ancestor reference. {% endhint %}
