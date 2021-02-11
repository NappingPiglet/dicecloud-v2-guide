# Damage Multipliers

A damage multiplier represents a character having an above average ability to withstand certain types of damage or being especially weak to certain types. These will appear on the stats page, with one card each for vulnerability, resistance and immunity.

## Components

### Name

The name of the damage multiplier. This is seperate from the actual damage type of tier of damage multiplication. At present, this is only visible from its parent property's card and the tree tab.

### Damage Type

What type of damage this damage multiplier affects. A full list of the different damage types and what they do can be found in the [SRD](https://www.5esrd.com/gamemastering/combat/#Damage_Types).

### Value \(Required\)

What the multiplier to damage of the selected types will be. Resistance is times 0.5, immunity is times 0 and vulnerability is times 2. In the event more than one value is present for a single damage type, all of them will be applied seperatly, so resistance and vulnerability produce a times 1 multiplier, and immunity plus anything else produces a times 0 multiplier.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Hidden Values

Note that all values listed here can only be accessed using the `#damageMultiplier.<valueName>` syntax from a child of the property.

### name

Returns the name of the damage multiplier.

### value

Returns 0.5 if the damage multiplier is set to resistance, 0 if it is set to immunity and 2 if it is set to vulnerability.
