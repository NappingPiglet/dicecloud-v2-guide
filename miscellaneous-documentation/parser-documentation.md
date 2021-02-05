# The Parser

DiceCloud V2 uses a custom parser that accepts all the common mathematical equations, such as addition, subtraction and exponents, as well as multiple functions. In text that accepts calculations, anything contained within `{}` will be parsed and only the final value of the parsing will display.

## Data Types

* Numbers
  * `54`
  * `3.14`
  * `NaN` \("not a number", can't be manually written but results from some invalid operations\)
  * `Infinity` \(can't be manually written but results from some invalid operations\)
* Strings
  * `"Hello, world!"`
  * `'Hello, world!'`
* Variables
  * `cantripDice`
  * `barbarian.level` \(access a sub-property of a variable\)
  * `#attribute` \(reference the nearest tree ancestor of the given type\)
* Booleans
  * `true`
  * `false`
* Arrays
  * `[1,2,3,4,5,6][index]` \(get the `index`th element in the array, starting from `1`\)

{% hint style="info" %}
If a variable doesn't exist, its value will default to `0`.
{% endhint %}

{% hint style="info" %}
Arrays must currently be defined in the same place they are accessed; an upcoming update will allow them to be defined in constants with the syntax `[1,2,3,4,5,6]`, and accessed later via `variable[index]`.
{% endhint %}

{% hint style="warning" %}
Ancestor reference variables \(e.g.`#attribute`\) are not currently implemented, and will be added in an upcoming update.
{% endhint %}

## Operators

### Basic Math

Dicecloud supports the following operators for basic math operations:

* `5 + 7` Add
* `5 - 7` Subtract
* `5 * 7` Multiply
* `5 / 7` Divide
* `5 ^ 7` Exponents
* `5 % 7` Modulus \(remainder\)

{% hint style="info" %}
Division by `0` will not result in an error, but will instead return `Infinity`.
{% endhint %}

{% hint style="warning" %}
The modulus operator `%` is intended but not currently functional due to a bug, and will be fixed in an upcoming update.
{% endhint %}

### Logic and Comparisons

Dicecloud supports the following operators for logical operations and comparisons:

* `5 == 7`  Equal \(also `5 = 7`\)
* `5 === 7` Strict equal
* `5 != 7` Not equal
* `5 !== 7` Strict not equal
* `5 > 7` Greater than
* `5 >= 7` Greater than or equal to
* `5 < 7` Less than
* `5 <= 7` Less than or equal to
* `true && false` Logical AND  \(also `true & false`\)
* `true || false` Logical OR \(also `true | false`\)

{% hint style="info" %}
The normal `==` and `!=` will convert types to check equality; for example, `5 == "5"` will return `true`.  The strict `===` and `!==` will not; for example, `5 === "5"` will return `false`.
{% endhint %}

### Conditional Operators

Dicecloud uses the following syntax for conditionals:

`condition ? ifTrue : ifFalse`

**Examples**

* `level >= 6 ? 2 : 1`
* `raging && hp.currentValue > 5 ? 5*barbarian.level : 0`

### Dice Rolls

Dicecloud allows dice rolls to be embedded into formulas using the following syntax:

* `d6` Roll a 6-sided die
* `4d6` Roll four 6-sided dice

**Examples**

* `2d20`
* `4d(3+level)`
* `cantripDice d8`

## Functions

### Absolute Value

The syntax `abs(number)` will return the absolute value of the number.

#### Examples

* `abs(9) == 9`
* `abs(-3) == 3`

### Square Roots

The syntax `sqrt(number)` will return the square root of the number.

#### Examples

* `sqrt(16) == 4`
* `sqrt(10) == 3.1622776601683795`

### Maximum

The syntax `max(A, B,...)` will return the greatest of the given numbers.

#### Examples

* `max(12, 6, 3, 168) == 168`

### Minimum

The syntax `min(A, B,...)` will return the smallest of the given numbers.

#### Examples

* `min(12, 6, 3, 168) == 3`

### Rounding

The syntax `round(number)` will return the value of the number, rounded to the nearest integer.

#### Examples

* `round(5.95) == 6`
* `round(5.5) == 6`
* `round(5.05) == 5`

### Flooring

The syntax `floor(number)` will return the value of the number, rounded down to the nearest integer.

#### Examples

* `floor(5.95) == 5`
* `floor(5.05) == 5`
* `floor(5) = 5`
* `floor(-5.5) == -6`

### Ceiling

The syntax `ceil(number)` will return the value of the number rounded up to nearest integer.

#### Examples

* `ceil(5.95) == 6`
* `ceil(5.05) == 6`
* `ceil(5) == 5`
* `ceil(-5.5) == -5`

### Truncating

The syntax `trunc(number)` returns the value of the number with the decimal part removed.

#### Examples

* `trunc(5.95) == 5`
* `trunc(5.05) == 5`
* `trunc(5) == 5`
* `trunc(-5.5) == -5`

### Sign

The syntax `sign(number)` will return positive 1 if the number is greater than 0, -1 if the number is less than 0 and 0 if the number is 0

#### Examples

* `sign(-3) == -1`
* `sign(3) == 1`
* `sign(0) == 0`

