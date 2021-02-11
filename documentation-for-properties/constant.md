# Constants

A constant is a property that will not be changeable by effects, but which can store arrays as well as normal numbers.

## Components

### Name

The name of the constant.

### Variable Name

The variable used to access the constant in calculation. Accepts alphanumeric characters and underscores, but not spaces or dashes.

### Value

The value of the constant. This cannot reference another variable, but can include an array. Note that array indexing starts at 1, unlike most programming languages.

## Accessible Values

Note that no value can be accessed using `<variableName>.<valueName>` currently. The syntax `<variableName>[n]` for positive integers n works if the constant has an array in the value however. All values listed here can be accessed using the syntax `#constant.<valueName>` from a child of the property.

### name

The name of the constant.

### variableName

The name of the variable used to access the constant.

### calculation

The number or array in the value field, parsed if it has math. Note that math is rarely present in this field as it cannot access variables.
