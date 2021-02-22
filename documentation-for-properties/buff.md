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

### name\*

The name of the buff.

### description\*

The text in the description field of the buff, unparsed.

### duration\*

Currently unused.

### applied\*

Returns true if the buff is applied. A buff will be applied if it is currently active on the character, while it will not be applied if it is a child of an action or spell that applies the buff.

### target\*

Returns 'self' if the buff's target field is set to self, 'every' if it is set to roll once and apply to each target, and 'each' if it is set to roll once for every target.

### durationSpent\*

Currently unused.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

