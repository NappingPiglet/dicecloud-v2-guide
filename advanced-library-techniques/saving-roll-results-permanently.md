# Saving Roll Results Permanently

When working with the roll syntax \(`4d6`\) in Dicecloud, rolls will recalculate any time a change is made to your sheet, even an unrelated one, which makes it difficult to permanently save the results of a roll to an attribute. In order to do so, a layer of indirection needs to be introduced.

{% hint style="info" %}
Note that this method only works if you can use an action to trigger the save.
{% endhint %}

Instead of setting your base value or effect directly to your roll, do the following:

* Set the base value of your attribute to the maximum roll result.
* Create an action with an attribute damage property in Set mode pointed at the attribute.
* Set the amount of the attribute damage to your roll.

Upon triggering the action, the result of the roll will be saved to the damage of your attribute, where it will be accessible with `attribute.currentValue`. This will lock the result in permanently until the action is triggered again, and prevent it from being recalculated.

{% hint style="warning" %}
Make sure to use Set mode for the attribute damage! Damage mode will set the damage itself to the result of your roll, which is harder to access, and will stack and give inaccurate results if the action is triggered multiple times.
{% endhint %}

If you need to have the value of your attribute be the resulting roll, as opposed to the `currentValue`, you can apply the roll saving method to a secondary attribute in Utility mode, and set your real attribute to the `currentValue` of the internal attribute.



