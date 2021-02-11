# Attribute Damage

Attribute damage is a way of causing an [action](action.md) or [attack](attackaction.md) to reduce an ability score, resource, or other attribute. They do nothing unless they are the child of an action in the tree, and only change the value of the attribute when you take that action.

## Components

### Attribute

The variable name of the attribute this property will affect.

### Damage

The amount that the attribute will be modified by or to. This can be either a number or calculation.

### Operation \(Required\)

What the attribute damage will do to the attribute.

* Damage
  * The attribute will have its value decremented by the value of the attribute damage.
* Set
  * The attribute will have its current value set to the value of the attribute damage.

### Target \(Required\)

The target of the attribute damage and the way that the damage will be calculated if a roll is involved in the damage field.

* Self
  * You are the victim of the attribute damage.
* Roll Once for Each Target
  * Each creature that the attribute damage effects will have the dice for the damage rolled separately.
* Roll once and Apply to Every Target
  * The dice will be rolled once and that value will be used for every creature the effect targets.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

Note that all values listed here can only be accessed using the `#adjustment.<valueName>` syntax from a child of the property. The syntax `#attributeDamage.<valueName>` and any variation on that syntax will not work.

### amount

This returns the string entered into the damage field, unparsed.

### target

This returns a string, containing the target of the attribute damage. Returns 'self' for self, 'each' for roll once for each target and 'every' for roll once and apply to every target.

### stat

This returns the variable name of the targeted attribute for the attribute damage.

### operation

This returns 'set' if the attribute damage is set to the set operation, and returns 'increment' if the attribute damage is set to the damage operation.

### amountResult

Returns an integer containing the parsed value of what is in the damage field. If a dice roll has been entered into the field, it will return a string instead, with all parsable portions of the string parsed.
