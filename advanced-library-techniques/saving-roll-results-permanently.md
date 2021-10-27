# Saving Roll Results Permanently

When working in Dicecloud, sometimes you'll want to store the result of a roll indefinitely. You might try setting an attribute's base value to use the roll syntax \(`4d6`\), but rolls of that nature will recalculate any time a change is made to your sheet, even an unrelated one. Instead, you should use an [Action](../documentation-for-properties/action.md) paired with the [Roll](../documentation-for-properties/roll.md) property.

{% hint style="info" %}
Note that this method only works if you can use an action to trigger the save. There is no known method for saving roll results permanently without an action.
{% endhint %}

Instead of setting the base value of an attribute or an effect to your desired roll, do the following:

* Set the base value of your attribute to the maximum roll result.
* Create an Action with a Roll property inside it, with the "Roll" field set to your roll formula.
* Create an [Attribute Damage](../documentation-for-properties/attribute-damage.md) property inside your action.
  * Set the "Attribute" field to your attribute, and the "Damage" field to your Roll's variable name.
  * Set the mode to "Set" and the target to "Self".

Upon triggering the action, the result of the roll will be saved to the damage of your attribute, where it will be accessible with `attribute.currentValue`. This will lock the result in permanently until the action is triggered again, and prevent it from being recalculated.

{% hint style="warning" %}
Make sure to use Set mode for the attribute damage! Damage mode will set the damage itself to the result of your roll, which is harder to access, and will stack and give inaccurate results if the action is triggered multiple times.
{% endhint %}

If you need to have the value of your attribute be the resulting roll, as opposed to using the attribute's`currentValue`, you can apply the roll saving method to a secondary attribute in Utility mode, and set your real attribute to the `currentValue` of the utility attribute.

