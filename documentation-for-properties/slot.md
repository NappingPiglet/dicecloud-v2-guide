# Slots

Slots are one of the single most powerful tools in DiceCloud V2. A slot on its own serves no function, but it can be filled from the character tab to add properties from libraries. These can be precisely controlled using tags and can reduce the time to make a character to a matter of seconds when set up properly.

## Components

### Name

The name of the slot, used to identify it on the character tab.

### Type

The type of property that this slot wants to fill it. Only properties who's type matches what you select here will appear in the dialogue box to fill the slot. If you leave this empty, then the only thing that limits what can fill the slot are tags and conditions.

### Tags Required

The tags that a property must have in order to fill the slot. You may add as many tags as you want here, but keep in mind that the property needs to match ALL the tags. Because they have additional functionality, the tags `inventory`, `equipment` and `carried` should generally be avoided in this field.

Selecting the plus button adds another row for tags, which have an additional option for Operation. This can be set to either OR or NOT. If set to OR, then the slot can be filled so long as the property filling it has at least one of these tags. If it is set to NOT, then any property that has at least one of the listed tags cannot be used to fill it.

### Quantity \(Required\)

How many properties can be put in the slot before it will stop accepting additional properties. Entering 0 means unlimited properties.

### Condition

When the condition inside this field is false, the slot will hide itself in the character tab and expanded view of the build card, meaning the only way to alter its contents will be the tree tab. This accepts both numbers and calculations, though numbers greater than 0 should be avoided as they are evaluated to true. Note that the contents of a slot who's condition becomes false still affect the sheet- condition only effects the user's ability to interact with the slot. To prevent the slot's children from affecting the sheet, a toggle should be used.

### Unique

This determines whether or not the same property can be added multiple times to a slot, or to the character as a whole. It defaults to "Each property inside this slot should be unique", which prevents the same property from being added to the slot multiple times. It can also be set to "Properties in this slot should be unique across the whole character", which prevents the same property from filling any slot again across the entire character.

{% hint style="info" %} This field defaults to "Each property inside this slot should be unique", but this field can be set to empty by using the X button on the right side of the field. {% endhint %}

{% hint style="info" %} Note that this means a given library node cannot be used multiple times. An exact copy of said node however, could be used after the original has been added. {% endhint %}

### Description

A description of the slot, which cannot be viewed outside of the tree. This field accepts markdown and HTML.

## Advanced

### Hide When Full

When this is set to true the slot will hide itself on the build card once it is full. It will still be visible in the expanded view. If the quantity is set to 0 the slot will remain visible on the build card, but will only show its children in the expanded view.

### Ignored

Currently serves no purpose. Intended to serve some role in a notification system later on.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the slot.

### description\*

The text of the description field, unparsed.

### slotType\*

The property type the slot expects. The string returned will be the one used to perform an ancestor reference to that property type.

### quantityExpected\*

The quantity of properties that the slot will accept at most.

### ignored\*

Returns true if the ignored field is set to true.

### slotCondition\*

Returns the string entered into the condition field, unparsed.

### hideWhenFull\*

Returns true if the hide when full field is set to true.

### quantityExpectedResult\*

Returns the parsed value of the quantity expected field.

### totalFilled\*

Returns the current quantity of properties that are filling the slot, with slot fillers filling up a number of properties equal to what is in their quantity field.

### spaceLeft\*

Returns the current number of properties that could be added to the slot before it is filled up.

### unique\*

Returns "uniqueInSlot" if the slot has the field Unique set to "Each property inside this slot should be unique" and returns "uniqueInCreature" if the field is set to "Properties in this slot should be unique across the whole character". If the field has been unset, it instead returns `#propertySlot.unique`.

{% hint style="warning" %}
All values marked with a \* can only be accessed using ancestor references.
{% endhint %}

{% hint style="info" %}
In order to perform an ancestor reference to a slot, the syntax is `#propertySlot` rather than `#slot`.
{% endhint %}

