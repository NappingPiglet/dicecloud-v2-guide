# Spell Lists

A spell list is a way to sort your spells, most often by which features gives you them. They will appear on the spells tab, with every spell property that is a child of them listed below them in a column.

## Components

### Name

The name of the spell list, which will appear at the top of the spell list in the spells tab.

### Variable Name

A variable name used to access information about this spell list in calculations. Currently has no functionality. Accepts both uppercase and lowercase Latin characters as well as underscores and numbers.

### Description

A description of the spell list, which will appear when you click on the spell list's name on the spells tab. This field accepts markdown, HTML, and calculations within {}.

### Maximum Prepared Spells

The maximum number of spells that can be prepared at one time in this spell list. Accepts both numbers and calculations. If left empty, the spell list will ignore spell prepared limits.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

Returns the name of the spell list.

### description\*

Returns the description of the spell list, unparsed.

### variableName\*

The variable name of the spell list.

### maxPrepared\*

The string in the maximum spells prepared field, unparsed.

### maxPreparedResult\*

Returns the string in the maximum spells prepared field, parsed.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

