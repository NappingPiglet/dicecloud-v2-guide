# Damage Multipliers

A damage multiplier represents a character having an above average ability to withstand certain types of damage or being especially weak to certain types. These will appear on the stats page, with one card each for vulnerability, resistance and immunity.

## Components

### Name

The name of the damage multiplier. This is separate from the actual damage type of tier of damage multiplication. At present, this is only visible from its parent property's card and the tree tab.

### Damage Type

What type of damage this damage multiplier affects. A full list of the different damage types and what they do can be found in the [SRD](https://www.5esrd.com/gamemastering/combat/#Damage_Types).

### Value \(Required\)

What the multiplier to damage of the selected types will be. Resistance is times 0.5, immunity is times 0 and vulnerability is times 2. In the event more than one value is present for a single damage type, all of them will be applied separately, so resistance and vulnerability produce a times 1 multiplier, and immunity plus anything else produces a times 0 multiplier.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the property.

### value\*

Returns 2 if the damage multiplier is set to vulnerability, 0.5 if it is set to resistance and 0 if it is set to immunity.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

## Unimplemented Functionality

### Exclude Tags

This will most likely cause the multiplier to not affect damage that has certain tags, such as `silver` or `magic` for resistance to non-magical B/P/S damage.

### Include Tags

This will most likely cause the multiplier to only affect damage that has certain tags, such as how a Rakshasa has vulnerability to piercing damage from good aligned creatures.

