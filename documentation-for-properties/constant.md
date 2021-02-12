# Constants

A constant is a variable that is invisible outside of the tree and cannot have its value use other variables. Unlike normal attributes however, constants can have arrays as their value, which can then be accessed using `<variableName>[n]` where n can be any positive number, so long as it isn't greater than the number of values in the array.

## Components

### Name

The name of the constant.

### Variable Name

The name of the variable used to access the constant in calculations. This can contain both uppercase and lowercase Latin characters, numbers and underscores, but not any other characters.

### Value

The value of the constant. This cannot reference another variable, or contain dice rolls but can include arrays.

## Accessible Values

### name

The name of the constant.

### variableName\*

Returns the variable name of the constant.

### calculation

Returns the string in the value field, parsed.

{% hint style="warning" %} Values marked with a \* can only be accessed using an ancestor reference. {% endhint %}
