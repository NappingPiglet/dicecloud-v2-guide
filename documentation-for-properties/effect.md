# Effects

An effect modifies an variable. These are used for things like giving yourself a base move speed or receiving a bonus to strength because of a feat.

## Components

### Name

The name of the effect. This will appear on the expanded view of the variables it applies to.

### Operation

What the effect does to the variables.

| Operation | Description |
| :--- | :--- |
| Base Value | This gives the variables a base value. In the event that more than one base value exists, it will use the highest number. |
| Add | This adds the effect's value to the variables. |
| Multiply | This multiplies the variables by the effect's value. |
| Minimum | This applies a minimum value after calculations but before attribute damage to the variables. If more than one minimum exists for a variable, the greatest one will be used. |
| Maximum | This applies a maximum value after calculations but before attribute damage to the variables. If more than one maximum exists for a variable, the lowest value will be used. |
| Set | This sets the value of the variables after calculations but before attribute damage. If more than one set exists for a variable, the greatest value will be used. This causes all non-set effects applied to the variable to be ignored. |
| Advantage | This indicates you have advantage on rolls involving the given variable. This only produces a visible result on skills, ability scores and modifiers at the moment. If applied to an ability score then all skills whose type is skill that rely on that ability will be marked as having advantage as well. |
| Disadvantage | This is the same as advantage, but instead marks you as having disadvantage on rolls. |
| Passive Bonus | This applies a bonus to the passive value of the variable. A variable will only show the passive bonus if at least one effect of this type is applied to it. A passive bonus is calculated as `10+<skillName>` and will appear next to the variable's name on the stats page. Currently, this only produces a visible effect on skills. |
| Fail | Marks you as automatically failing all rolls involving the given variable. Functions like advantage in all other regards. |
| Conditional Benefit | Marks the variable in question with an asterisk on the stats page. This is used to indicate an ability that provides some benefit only under certain circumstances, such as magic resistance. This otherwise functions in the same way as advantage. |

### Stats

The names of the variables that the effect will impact. You can't pass it a specific component of a variable, such as `constitution.modifier`.

### Value

What the value of the modification is. This field cannot be edited for advantage, disadvantage, fail and conditional benefit type effects. This can store either a number or a calculation.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the effect.

### operation\*

Returns the operation of the effect.

| Operation | Return Value |
| :--- | :--- |
| Base Value | base |
| Add | add |
| Multiply | mul |
| Minimum | min |
| Maximum | max |
| Set | set |
| Advantage | advantage |
| Disadvantage | disadvantage |
| Passive Bonus | passive |
| Fail | fail |
| Conditional Bonus | conditional |

### calculation\*

The string in the calculation field, unparsed.

### result\*

The string in the calculation field, parsed. If dice rolls are included, all non-dice components are parsed.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

