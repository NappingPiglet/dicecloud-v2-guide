# The Parser

DiceCloud V2 uses a custom parser that accepts all the common mathematical equations, such as addition, subtraction and exponents, as well as multiple functions. In text that accepts calculations, anything contained within `{}` will be parsed and only the final value of the parsing will display.

## Functions

### If-Else Statements

V2 uses a ternary if statement, with the syntax of `conditional ? truthy : falsey`. Conditions can have ANDs using `&` or `&&`, ORs with `|` or `||`, NOT with `!` and both `==` and `===` forms of equality operators.

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

