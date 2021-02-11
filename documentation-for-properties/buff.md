# Buffs

A buff is an effect that is given to a creature as a result of an action. These primarily will store children that serve to grant features or modify attributes. These are intended to represent a temporary addition or subtraction to a creature's power or abilities.

## Components

### Name

The name of this buff, which is displayed next to the buff icon on the stats page.

### Description

A long description of the buff, which will appear when you click on the buff's name on the stats tab. This field accepts markdown, HTML, and calculations within {}.

### Target \(Required\)

The target of the buff and the way that all rolled effects of the buff's children will be calculated.

* Self
  * You are the victim of the attribute damage.
* Roll Once for Each Target
  * Each creature that the buff effects will have the dice for the children rolled separately.
* Roll once and Apply to Every Target
  * The dice will be rolled once and that value will be used for every creature the effect targets.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

Note that all of the values listed here can only be accessed using the `#buff.<valueName>` syntax from a child of the property.

### name

The name of buff.

### description

The text entered into the description field of the buff, unparsed.

### duration

Currently an unused value.

### applied

Returns true if the buff is currently applied, and returns false if it isn't applied. If the buff is a child of an action, it is not applied.

### target
This returns a string, containing the target of the buff. Returns 'self' for self, 'each' for roll once for each target and 'every' for roll once and apply to every target.

### durationSpent

Currently an unused value.
