# Damage

Damage represents your character suffering injury in some form or another. A damage component automatically calculates and applies damage when an action is taken, and must be a child of the action that applies the damage.

## Components

### Damage

The damage field controls how much damage will be dealt by this property. This accepts numbers or calculations, and will usually include at least one dice roll.

### Damage Type \(Required\)

What type the damage is. A full list of the different damage types and what they do can be found in the [SRD](https://www.5esrd.com/gamemastering/combat/#Damage_Types). Healing is also included in DiceCloud, which represents an effect that restores a creature's physical or mental state. In this case, the damage field instead represents how many hit points the creature will regain.

### Target \(Required\)

The target of the buff and the way that all rolled effects of the buff's children will be calculated.

* Self
  * You are the victim of the attribute damage.
* Roll Once for Each Target
  * Each creature that the buff effects will have the dice for the children rolled seperately.
* Roll once and Apply to Every Target
  * The dice will be rolled once and that value will be used for every creature the effect targets.
  
### Tags

Tags used to control which slots this property can be added to. This will usually be left blank unless you're making a library.
