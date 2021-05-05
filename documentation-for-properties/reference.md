# References

References are a unique property in that you cannot have them on a character sheet. A reference exists in a library, and when you create it you link another property form a library to the reference. Then, when you add that reference to a character sheet, it gets immediately replaced with the property linked to it.

{% hint style="warning" %}
In order to limit the strain that references can place on DiceCloud's database, there is a maximum depth of 10 references. What this means is that if a reference refers to another property that contains a reference as a child, it will still add that reference. If this happens 10 times however, it will no longer add the reference.
{% endhint %}

## Components

### Link

This is the only property of a reference. When you click on this, it will prompt you to select another property from a library. After you select a property and click confirm, a string of characters will appear in this box. This string is a reference to that property, and though it is meaningless to the user in most cases, it is what allows these to work.

## Accessible Values

Because a reference can only exist within a library, none of it's values can be accessed using either variable name or ancestor references. For completeness however, their internal values are still listed here.

### ref

This contains an object, which replaces the reference when it is added to a character.

### cache

This contains denormalised information about the object in the reference, including errors and the library it originates from.
