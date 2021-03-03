# Parser Documentation

DiceCloud V2 uses a custom parser that accepts all the common mathematical equations, such as addition, subtraction and exponents, as well as multiple functions. In text that accepts calculations, anything contained within `{}` will be parsed and only the final value of the parsing will display.

## Data Types

<table>
  <thead>
    <tr>
      <th style="text-align:left">Data Type</th>
      <th style="text-align:left">Examples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Numbers</td>
      <td style="text-align:left">
        <p><code>54</code>
        </p>
        <p><code>3.14</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Strings</td>
      <td style="text-align:left">
        <p><code>&quot;Hello, world!&quot;</code>
        </p>
        <p><code>&apos;Hello, world!&apos;</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Booleans</td>
      <td style="text-align:left">
        <p><code>true</code>
        </p>
        <p><code>false</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Arrays</td>
      <td style="text-align:left">
        <p><code>[1,2,3,4,5,6][index]</code>
        </p>
        <p><code>[1,2,3,4,5,6]</code> (constants only)</p>
        <p><code>arrayConstant[index]</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Variables</td>
      <td style="text-align:left">
        <p><code>cantripDice</code>
        </p>
        <p><code>barbarian.level</code> (sub-properties)</p>
        <p><code>#attribute</code> (ancestor reference by type)</p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
If a variable doesn't exist, its value will default to `0`.
{% endhint %}

{% hint style="info" %}
Array indexes start from `1`.
{% endhint %}

{% hint style="info" %}
Arrays must normally be declared in the same place they are accessed \(the first syntax example\), with the exception of declaring an array in a constant, which allows for storing non-numeric data types.
{% endhint %}

## Operators

### Basic Math

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Syntax</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Add</td>
      <td style="text-align:left"><code>5 + 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Subtract</td>
      <td style="text-align:left"><code>5 - 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Multiply</td>
      <td style="text-align:left"><code>5 * 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Divide</td>
      <td style="text-align:left"><code>5 / 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Exponents</td>
      <td style="text-align:left"><code>5 ^ 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Modulus (remainder)</td>
      <td style="text-align:left"><code>5 % 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Dice Rolls</td>
      <td style="text-align:left">
        <p><code>d6</code>
        </p>
        <p><code>2d20</code>
        </p>
        <p><code>cantripDice d8</code>
        </p>
        <p><code>4d(3+level)</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
Division by `0` will not result in an error, but will instead return `Infinity`.
{% endhint %}

{% hint style="info" %}
Dice rolls can use any variable or equation on either side of the `d` operator. They will be rerolled whenever the property using them is recalculated; if you want to save the result of a roll indefinitely, see [Saving Roll Results Permanently](../advanced-library-techniques/saving-roll-results-permanently.md).
{% endhint %}

### Logic and Comparisons

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Syntax</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Equal</td>
      <td style="text-align:left">
        <p><code>5 = 7</code>
        </p>
        <p><code>5 == 7</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Strict equal</td>
      <td style="text-align:left"><code>5 === 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Not equal</td>
      <td style="text-align:left"><code>5 != 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Strict not equal</td>
      <td style="text-align:left"><code>5 !== 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Greater than</td>
      <td style="text-align:left"><code>5 &gt; 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Greater than or equal to</td>
      <td style="text-align:left"><code>5 &gt;= 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Less than</td>
      <td style="text-align:left"><code>5 &lt; 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Less than or equal to</td>
      <td style="text-align:left"><code>5 &lt;= 7</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Logical AND</td>
      <td style="text-align:left">
        <p><code>true &amp; false</code>
        </p>
        <p><code>true &amp;&amp; false</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Logical OR</td>
      <td style="text-align:left">
        <p><code>true | false</code>
        </p>
        <p><code>true || false</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Conditional</td>
      <td style="text-align:left"><code>condition ? ifTrue : ifFalse</code>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
The normal `==` and `!=` will convert types to check equality; for example, `5 == "5"` will return `true`. The strict `===` and `!==` will not; for example, `5 === "5"` will return `false`.
{% endhint %}

{% hint style="info" %}
For the logical operators `&&` and `||`, as well as for the conditional operator `? :` and built-in condition checks like for toggles, most values will be considered equivalent to `true`, except for the following:

* `false`
* `0` and all equivalent values
* `NaN` \(results from some calculation errors\)
* Empty strings \(`""` and `''`\)
{% endhint %}

## Functions

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Syntax</th>
      <th style="text-align:left">Examples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Absolute Value</td>
      <td style="text-align:left"><code>abs(number)</code>
      </td>
      <td style="text-align:left">
        <p><code>abs(9) == 9</code>
        </p>
        <p><code>abs(-3) == 3</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Square Root</td>
      <td style="text-align:left"><code>sqrt(number)</code>
      </td>
      <td style="text-align:left">
        <p><code>sqrt(16) == 4</code>
        </p>
        <p><code>sqrt(10) == 3.1622776601683795</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Maximum</td>
      <td style="text-align:left"><code>max(number, ...)</code>
      </td>
      <td style="text-align:left"><code>max(12, 6, 3, 168) == 168</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Minimum</td>
      <td style="text-align:left"><code>min(number, ...)</code>
      </td>
      <td style="text-align:left"><code>min(12, 6, 3, 168) == 3</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Round (round to nearest whole)</td>
      <td style="text-align:left"><code>round(number)</code>
      </td>
      <td style="text-align:left">
        <p><code>round(5.95) == 6</code>
        </p>
        <p><code>round(5.5) == 6</code>
        </p>
        <p><code>round(5.05) == 5</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Floor (round down)</td>
      <td style="text-align:left"><code>floor(number)</code>
      </td>
      <td style="text-align:left">
        <p><code>floor(5.95) == 5</code>
        </p>
        <p><code>floor(5.05) == 5</code>
        </p>
        <p><code>floor(5) = 5</code>
        </p>
        <p><code>floor(-5.5) == -6</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Ceiling (round up)</td>
      <td style="text-align:left"><code>ceil(number)</code>
      </td>
      <td style="text-align:left">
        <p><code>ceil(5.95) == 6</code>
        </p>
        <p><code>ceil(5.05) == 6</code>
        </p>
        <p><code>ceil(5) == 5</code>
        </p>
        <p><code>ceil(-5.5) == -5</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Truncate (round toward 0)</td>
      <td style="text-align:left"><code>trunc(number)</code>
      </td>
      <td style="text-align:left">
        <p><code>trunc(5.95) == 5</code>
        </p>
        <p><code>trunc(5.05) == 5</code>
        </p>
        <p><code>trunc(5) == 5</code>
        </p>
        <p><code>trunc(-5.5) == -5</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Sign</td>
      <td style="text-align:left"><code>sign(number)</code>
      </td>
      <td style="text-align:left">
        <p><code>sign(-3) == -1</code>
        </p>
        <p><code>sign(3) == 1</code>
        </p>
        <p><code>sign(0) == 0</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Table Lookup</td>
      <td style="text-align:left"><code>tableLookup(array, number)</code>
      </td>
      <td style="text-align:left">
        <p><code>tableLookup([100, 300, 900], 457) == 2</code>
        </p>
        <p><code>tableLookup([100, 300, 900], 23) == 0</code>
        </p>
        <p><code>tableLookup([100, 300, 900, 1200], 900) == 3</code>
        </p>
        <p><code>tableLookup([100, 300], 594) == 2</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>

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

