# Class Levels

A class level represents one tier of ability in a certain skill set. These appear on the character tab, beneath your level.

## Components

### Level \(Required\)

The numeric level you have in this class. If more than one level value exists for a given variable name, the highest level version of the class will override all other class level components that use the same variable. This field doesn't accept calculations.

### Name

The name of the class. This appears next to the level of the class on the character tab.

### Variable Name \(Required\)

The variable name used to access information about the class. This accepts both uppercase and lowercase Latin characters, numbers and underscores, but not characters such as spaces.

### Description

The description of the class. This field accepts markdown, HTML, and calculations within {}.

### Condition

A condition to check if you can take levels in this class. Unless you are making a library, this can be left blank. For this class level to be added to a slot, this condition must evaluate to true.

{% hint style="info" %}
One useful example of a condition is `<classVariableName>.level==<classLevel>-1`, which will only allow you to take this particular level if you already had taken the previous level in the class.
{% endhint %}

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name

The name of the class.

### level

The current level you have in the class

### description\*

The text entered into the description field of the class level, unparsed.

### variableName\*

The text entered into the variable name field of the class level.

### slotFillerCondition\*

The text entered into the condition field, unparsed.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

