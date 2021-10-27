# Constants

A constant is a variable that is invisible outside of the tree and cannot have its value use other variables. Constants can also not be targeted by effects. Unlike normal attributes however, constants can store non-numeric data types such as strings, booleans, and arrays. This is most notable when using an array as its value, which can then be accessed using `<variableName>[n]`, rather than needing to define your array in the same place it's used \(see [Parser Documentation](../creating-a-library/parser-documentation.md#data-types)\).

## Components

### Name

The name of the constant.

### Variable Name

The name of the variable used to access the constant in calculations. This can contain both uppercase and lowercase Latin characters, numbers and underscores, but not any other characters.

### Value

The value of the constant. This cannot reference another variable, or contain dice rolls but can include arrays.

<p class="hint info">
One other unique property of constants is that they can never be overwritten, even by other constants that use the same variable name later in the tree. This means that they are unique in that they are the only property that will use the highest instance in the tree as their base value rather than the lowest instance.
</p>

## Accessible Values

### name

The name of the constant.

### variableName\*

Returns the variable name of the constant.

### calculation\*

Returns the string in the value field, parsed.

<p class="hint warning">
All values marked with a \* can only be accessed using an ancestor reference.
</p>

