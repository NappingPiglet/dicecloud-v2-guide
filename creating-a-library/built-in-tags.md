# Built-in Tags

Dicecloud V2 has some built-in property tags with special functionality. This page is a listing of all currently available built-in tags.

| Tag Name | Description |
| :--- | :--- |
| `attack` | Automatically added to all [Attack](../documentation-for-properties/attack-action.md) properties by default. |
| `base` | Marks a library item as a base to be imported with the default Base slot. |
| `carried` | When moving an item to the Carried list, marks an ancestor they should be put in. |
| `equipment` | When moving an item to the Equipped list, marks an ancestor they should be put in. |
| `inventory` | Present in Dicecloud's code, but currently unused. |

{% hint style="info" %}
The `carried` and `equipment` tags allow for managing inventory organization when working with the Carried and Equipped lists. By default, items will be moved to the top level of the tree when moved to either of these lists from a container. If the container is inside a property tagged appropriately, they will be made children of that property instead.
{% endhint %}

