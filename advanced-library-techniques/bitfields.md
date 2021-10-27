# Bitfields

A fairly common advanced technique in programming is the use of a "bitfield"; that is, storing multiple booleans in a single number, by using each bit of that number's binary representation as a boolean. This technique can be used in Dicecloud to reduce the number of attributes needed to store a large amount of related booleans flags, for example tracking which of the possible numbers have been selected for standard array ability scores.

## Application

If you want to use bitfields in your libraries, you can use the following formulas, replacing `bitfield` with the variable name your bitfield is stored in. An [Effect](../documentation-for-properties/effect.md) in Add mode can be substituted for the "set" formula by setting the effect target to `bitfield` and the value to the right-hand side of the `+`.

| Operation | Formula | Example for n = 4 |
| :--- | :--- | :--- |
| Set the `n`th boolean | `bitfield + 2^(n-1)` | `bitfield + 8` |
| Get the `n`th boolean | `floor(bitfield/(2^(n-1))) % 2` | `floor(bitfield/8) % 2` |

## Theory

**This technique involves a lot of complicated math. If you just want to use this technique and don't care about the theory behind it, you can safely skip the rest of this page.**

Some example code for using bitfields in a normal programming language might look something like this:

```javascript
// -- without bitfields -- //
const bool1 = true
const bool2 = false
const bool3 = true
const bool4 = false
const bool5 = true
const bool6 = false

if(bool4) {
  // do something
}

// -- with bitfields -- //
const bools = 0b010101

if(bools & 0b001000) {
  // do something
}
```

This can both reduce storage space and code clutter if used effectively, though it can also decrease readability if someone unfamiliar with the technique is working with your code. In essence, it boils down to two operations: the bitwise OR, and the bitwise AND.

```javascript
let bools = 0b000000

bools = bools | 0b001000  // Set the fourth boolean to true
truth = bools & 0b001000  // Check if the fourth boolean is true
```

However, Dicecloud has one major roadblock to applying this technique - it doesn't support bitwise operators! So how can we apply this clever technique to our libraries? As usual with code and math, there's a workaround.

### Workaround: Bitwise OR

The easiest part of this equation is how to emulate the use of bitwise OR for setting bits in our bitfield. Since binary works on powers of 2, emulating it is as simple as adding to our number. Let's say we want to set the 4th bit - all we need to do is add `2^3`, or to simplify a bit, add 8. You can also unset a bit by subtracting 8!

```javascript
Effect:
| Add
| bitfield
| +8
```

Note that there are a couple caveats here:

* Make sure you don't try to set the same bit twice! If we were using a real bitwise OR here, we wouldn't have to worry about it, since setting a bit that's already set would do nothing, but since we're adding, it will end up messing things up a lot.
* You might be wondering why `2^3` to get the 4th bit, rather than `2^4`. This is because the 1st bit is actually a value of 1, or `2^0`. This will be important later.

### Workaround: Bitwise AND

This is where things get complicated. You might be inclined to think that checking whether a bit is set is as simple as setting the bit, right? Well, it's not. It's much, much more difficult.

Trying to access an arbitrary bit in our number is too complicated. So we want to modify our bitfield so that the first \(lowest\) bit is the one we need to check. This can be accomplished with a right shift:

```javascript
// this method for accessing the fourth bit...
truth = oldBF & 8

// ... is equivalent to this method
newBF = oldBF >> 3
truth = newBF & 1
```

But Dicecloud doesn't have a right shift operator either. Luckily for us, a right shift is roughly equivalent to division by a power of two. So to access our fourth bit, we can use the following:

```javascript
newBF = floor(oldBF / 8)
truth = newBF & 1
```

And to finally get that naughty bitwise AND out of there, we can replace it with a check for whether the number is even or odd, using the modulo operator. If the number is odd - in other words, if the remainder of dividing it by 2 is 1 - our bit is set. That means our final equation comes out to:

```javascript
truth = floor(bitfield / 8) % 2
```

### Workaround: Modulus

{% hint style="danger" %}
This section is now obsolete as the modulus operator has been fully implemented. It has been left here for those interested in the math behind the original solution.
{% endhint %}

Unfortunately, our troubles don't end there, because due to an implementation oversight, Dicecloud doesn't have modulo either... yet. It will soon, which will make this process much cleaner, but for now, we need another layer of workarounds.

Luckily, there's a simple mathematical equivalent to modulo that uses only operators and functions that Dicecloud actually has available right now:

```javascript
x % y == x - y*floor(x/y)
```

Since the right-hand side of our modulo operator \(`y`\) is always 2, expanding our current solution with that results in the following:

```javascript
floor(bitfield/8) - 2*floor(floor(bitfield/8)/2)
```

We can clean up and reduce that a bit further by removing the nested `floor`s and combining the divisions, which results in the following final equation:

```javascript
floor(bitfield/8) - 2*floor(bitfield/16)
```

