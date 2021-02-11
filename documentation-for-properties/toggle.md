# Toggles

A toggle allows you to enable or disable other properties in response to a condition. Only children of the toggle can be affected directly by it.

## Components

### Name

The name of the toggle.

### Enabled/Disabled \(Required\)

Is the toggle enabled or disabled? When set to calculated, it will be enabled when the condition field evaluates to true and disabled when it evaluates to false.

### Condition

A calculation to test if the toggle should be enabled or disabled. When the toggle is not set to calculated, this will not be visible.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

Note that all values listed here can only be accessed using the `#toggle.<valueName>` field from a child of the property.

### name

The name of the toggle.

### disabled

Returns true if the toggle is always disabled. Note that this property will technically never return true because it will never be visible outside of the tree if the toggle is disabled.

### enabled

Returns true if the toggle is always enabled.

### condition

Returns the string entered into the condition field.

### toggleResult

Returns true if the toggle is enabled, and false if it is disabled.
