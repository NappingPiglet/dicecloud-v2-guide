# Constants

<<<<<<< HEAD
A constant is a property that will not be changeable by effects, but which can store arrays as well as normal numbers.
=======
A constant is a variable that is invisible outside of the tree and cannot have its value use other variables. Unlike normal attributes however, constants can store non-numeric data types such as strings, booleans, and arrays. This is most notable when using an array as its value, which can then be accessed using `<variableName>[n]`, rather than needing to define your array in the same place it's used \(see [Parser Documentation](../creating-a-library/parser-documentation.md#data-types)\).
>>>>>>> origin/content-that-hasnt-gone-live

## Components

### Name

The name of the constant.

### Variable Name

<<<<<<< HEAD
The variable used to access the constant in calculation. Accepts alphanumeric characters and underscores, but not spaces or dashes.

### Value

The value of the constant. This cannot reference another variable, but can include an array. Note that array indexing starts at 1, unlike most programming languages.

## Accessible Values

Note that no value can be accessed using `<variableName>.<valueName>` currently. The syntax `<variableName>[n]` for positive integers n works if the constant has an array in the value however. All values listed here can be accessed using the syntax `#constant.<valueName>` from a child of the property.

=======
The name of the variable used to access the constant in calculations. This can contain both uppercase and lowercase Latin characters, numbers and underscores, but not any other characters.

### Value

The value of the constant. This cannot reference another variable, or contain dice rolls but can include arrays.

## Accessible Values

>>>>>>> origin/content-that-hasnt-gone-live
### name

The name of the constant.

<<<<<<< HEAD
### variableName

The name of the variable used to access the constant.

### calculation

The number or array in the value field, parsed if it has math. Note that math is rarely present in this field as it cannot access variables.
=======
### variableName\*

Returns the variable name of the constant.

### calculation

Returns the string in the value field, parsed.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

>>>>>>> origin/content-that-hasnt-gone-live
