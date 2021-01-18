# Roll

Unfortunantly, the roll property currently has no functionality. However, we can learn it's functionality from comments in the DiceCloud code as well as the field names. The same is true of [saving throws](https://katrinakitten.gitbook.io/dicecloud-v2-guide/documentation-for-properties/savingthrow).

The roll component is used to automate rolling some quantity of dice in response to an action. The intended use of this seems to be activating abilities in response to certain dice rolls, at least from the comments.

> \* \# Rolls are resolved in one of two ways:  
> \* Regular rolls:  
> \* The target number is computed in the target's context  
> \* The roll is computed in the action taker's context  
> \* If the roll meets or exceeds the target number, the adjustments and buffs  
> \* are applied

## Components

### Roll

A calculation for the dice that are to be rolled, which will likely include dice rolls in the calculation.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.
