# Attribute Damage

Attribute damage is a way of causing an [action](action.md) or [attack](attack-action.md) to reduce an ability score, resource, or other attribute. They do nothing unless they are the child of an action in the tree, and only change the value of the attribute when you take that action.

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

### amount\*

Returns the string in the amount field, unparsed.

### target\*

Returns 'self' if the target of the attribute damage is set to self, 'each' if it is set to to roll once for each enemy, and returns 'every' if it is set to roll once and apply to every enemy.

### stat\*

Returns the variable name of the attribute this attribute damage affects.

### operation\*

Returns 'set' if the operation is set to set and returns 'increment' if it is set to damage.

### amountResult\*

Returns the parsed value of the amount field. If dice rolls are included, then all non-dice roll components are parsed.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

{% hint style="info" %}

Ancestor references to an attribute damage property must be written as `#adjustment`, rather than `#attributeDamage`.

{% endhint %}


