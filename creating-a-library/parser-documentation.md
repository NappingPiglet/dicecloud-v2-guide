# Parser Documentation

DiceCloud V2 uses a custom parser that accepts all the common mathematical equations, such as addition, subtraction and exponents, as well as multiple functions. In text that accepts calculations, anything contained within `{}` will be parsed and only the final value of the parsing will display.

## Data Types

| Data Type | Examples                                                                                                                                       |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Numbers   | <p><code>54</code></p><p><code>3.14</code></p>                                                                                                 |
| Strings   | <p><code>"Hello, world!"</code></p><p><code>'Hello, world!'</code></p>                                                                         |
| Booleans  | <p><code>true</code></p><p><code>false</code></p>                                                                                              |
| Arrays    | <p><code>[1,2,3,4,5,6][index]</code></p><p><code>[1,2,3,4,5,6]</code> (constants only)</p><p><code>arrayConstant[index]</code></p>             |
| Variables | <p><code>cantripDice</code></p><p><code>barbarian.level</code> (sub-properties)</p><p><code>#attribute</code> (ancestor reference by type)</p> |

<p class="hint info">
If a variable doesn't exist, its value will default to `0`, however this is not true for inline calculations. Inline calculations will break if the variable doesn't exist.
</p>

<p class="hint info">
Array indexes start from `1`.
</p>

<p class="hint info">
Arrays must normally be declared in the same place they are accessed (the first syntax example), with the exception of declaring an array in a constant, which allows for storing non-numeric data types.
</p>

## Operators

### Basic Math

| Name                | Syntax                                                                                                          |
| ------------------- | --------------------------------------------------------------------------------------------------------------- |
| Add                 | `5 + 7`                                                                                                         |
| Subtract            | `5 - 7`                                                                                                         |
| Multiply            | `5 * 7`                                                                                                         |
| Divide              | `5 / 7`                                                                                                         |
| Exponents           | `5 ^ 7`                                                                                                         |
| Modulus (remainder) | `5 % 7`                                                                                                         |
| Dice Rolls          | <p><code>d6</code></p><p><code>2d20</code></p><p><code>cantripDice d8</code></p><p><code>4d(3+level)</code></p> |

<p class="hint info">
Division by `0` will not result in an error, but will instead return `Infinity`.
</p>

<p class="hint info">
Dice rolls can use any variable or equation on either side of the `d` operator. They will be rerolled whenever the property using them is recalculated; if you want to save the result of a roll indefinitely, see [Saving Roll Results Permanently](../advanced-library-techniques/saving-roll-results-permanently.md).
</p>

### Logic and Comparisons

| Name                     | Syntax                                                                           |
| ------------------------ | -------------------------------------------------------------------------------- |
| Equal                    | <p><code>5 = 7</code></p><p><code>5 == 7</code></p>                              |
| Strict equal             | `5 === 7`                                                                        |
| Not equal                | `5 != 7`                                                                         |
| Strict not equal         | `5 !== 7`                                                                        |
| Greater than             | `5 > 7`                                                                          |
| Greater than or equal to | `5 >= 7`                                                                         |
| Less than                | `5 < 7`                                                                          |
| Less than or equal to    | `5 <= 7`                                                                         |
| Logical AND              | <p><code>true &#x26; false</code></p><p><code>true &#x26;&#x26; false</code></p> |
| Logical OR               | <p><code>true | false</code></p><p><code>true || false</code></p>                |
| Conditional              | `condition ? ifTrue : ifFalse`                                                   |

<p class="hint info">
The normal `==` and `!=` will convert types to check equality; for example, `5 == "5"` will return `true`. The strict `===` and `!==` will not; for example, `5 === "5"` will return `false`.
</p>

<p class="hint info">
For the logical operators `&&` and `||`, as well as for the conditional operator `? :` and built-in condition checks like for toggles, most values will be considered equivalent to `true`, except for the following:

* `false`
* `0` and all equivalent values
* `NaN` (results from some calculation errors)
* Empty strings (`""` and `''`)
</p>

## Functions

| Name                           | Syntax                       | Examples                                                                                                                                                                                                                                 |
| ------------------------------ | ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Absolute Value                 | `abs(number)`                | <p><code>abs(9) == 9</code></p><p><code>abs(-3) == 3</code></p>                                                                                                                                                                          |
| Square Root                    | `sqrt(number)`               | <p><code>sqrt(16) == 4</code></p><p><code>sqrt(10) == 3.1622776601683795</code></p>                                                                                                                                                      |
| Maximum                        | `max(number, ...)`           | `max(12, 6, 3, 168) == 168`                                                                                                                                                                                                              |
| Minimum                        | `min(number, ...)`           | `min(12, 6, 3, 168) == 3`                                                                                                                                                                                                                |
| Round (round to nearest whole) | `round(number)`              | <p><code>round(5.95) == 6</code></p><p><code>round(5.5) == 6</code></p><p><code>round(5.05) == 5</code></p>                                                                                                                              |
| Floor (round down)             | `floor(number)`              | <p><code>floor(5.95) == 5</code></p><p><code>floor(5.05) == 5</code></p><p><code>floor(5) = 5</code></p><p><code>floor(-5.5) == -6</code></p>                                                                                            |
| Ceiling (round up)             | `ceil(number)`               | <p><code>ceil(5.95) == 6</code></p><p><code>ceil(5.05) == 6</code></p><p><code>ceil(5) == 5</code></p><p><code>ceil(-5.5) == -5</code></p>                                                                                               |
| Truncate (round toward 0)      | `trunc(number)`              | <p><code>trunc(5.95) == 5</code></p><p><code>trunc(5.05) == 5</code></p><p><code>trunc(5) == 5</code></p><p><code>trunc(-5.5) == -5</code></p>                                                                                           |
| Sign                           | `sign(number)`               | <p><code>sign(-3) == -1</code></p><p><code>sign(3) == 1</code></p><p><code>sign(0) == 0</code></p>                                                                                                                                       |
| Table Lookup                   | `tableLookup(array, number)` | <p><code>tableLookup([100, 300, 900], 457) == 2</code></p><p><code>tableLookup([100, 300, 900], 23) == 0</code></p><p><code>tableLookup([100, 300, 900, 1200], 900) == 3</code></p><p><code>tableLookup([100, 300], 594) == 2</code></p> |

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

### Table Lookup

The syntax `tableLookup([number, number, ...], number)` will return the index of the last number that is less than the second parameter of the function from the array given. This array can also be a constant.

#### Examples

* `tableLookup([100, 300, 900], 457) == 2`
* `tableLookup([100, 300, 900], 23) == 0`
* `tableLookup([100, 300, 900, 1200], 900) == 3`
* `tableLookup([100, 300], 594) == 2`
