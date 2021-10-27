# Saving Throws

A saving throw is a property that should almost always be a child of an [action](action.md), [attack](attack-action.md) or [spell](spell.md). A saving throw has a DC and a save. When the action it is a child of is taken, a d20 will be rolled and the modifier from the saving throw it uses will be added to that result. If the saving throw is passed, then children of the save will not be applied. If it is failed, then its children will be applied, which will often include conditions or damage.

## Components

### Name

The name of the saving throw.

### DC

The minimum roll needed to avoid suffering negative effects. Accepts numbers and calculations.

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

### target\*

Returns 'self' if the target of the saving throw is set to self, 'each' if it is set to roll once for each target and 'every' if it is set to roll once and apply to every target.

### dcResult\*

The DC of the saving throw, parsed. If dice rolls are included, then all non-dice rolls are parsed.

{% hint style="warning" %}
All values marked by a \* can only be accessed using an ancestor reference.
{% endhint %}

