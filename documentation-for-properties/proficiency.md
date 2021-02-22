# Proficiencies

A proficiency represents your character having training, natural talent or uncanny luck when performing certain kinds of tasks.

## Components

### Name

The name of this proficiency. This is separate from what it actually indicates proficiency in, and only appears if you expand the skill it affects.

### Skills

A list of the variable names of all skills you want this property to affect.

* **Note:** The variables `allSaves` and `allChecks` exist in the code, but have no functionality at the moment.

### Proficiency \(Required\)

The level of proficiency this property grants. Proficient means you can add your proficiency bonus to checks with the skill, half proficient means you can add half your proficiency bonus to checks, and double proficiency bonus means you can add twice your proficiency bonus to checks.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the proficiency.

### value\*

Returns 0.5 if the property grants half proficiency, 1 if it grants normal proficiency and 2 if it grants double proficiency.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

