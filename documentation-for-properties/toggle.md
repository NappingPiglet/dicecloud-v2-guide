# Toggles

A toggle allows you to enable or disable other properties in response to a condition. Only children of the toggle can be affected directly by it.

## Components

### Name

The name of the toggle.

### Enabled/Disabled/Conditional \(Required\)

Is the toggle enabled or disabled? When set to calculated, it will be enabled when the condition field evaluates to true and disabled when it evaluates to false.

### Condition

A calculation to test if the toggle should be enabled or disabled. When the toggle is not set to calculated, this will not be visible.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the toggle.

### disabled\*

Returns true if the toggle is disabled.

### enabled\*

Returns true if the toggle is enabled.

### condition\*

Returns the string in the toggle's condition field.

### toggleResult\*

Returns true if the condition field is evaluated to true.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

