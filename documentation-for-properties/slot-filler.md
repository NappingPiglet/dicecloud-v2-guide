# Slot Fillers

A slot filler is a property that is intended to allow for greater control over filling slots, and will usually have additional properties as children that grant features or other effects.

## Components

### Icon

Select an icon to represent this slot filler on the character page. Icons come from [game-icons.net](https://game-icons.net) and will change their color to match the slot filler's color.

### Name

The name of the slot filler, visible under the slot it is added to from the character page.

### Description

A description of the slot filler, which will appear when you click on the slot filler's name on the character tab. This field accepts markdown, HTML, and calculations within {}.

### Picture URL

A URL to an image to represent this slot filler, which will be visible when in the dialogue to add it to a slot. Currently bugged \(?\), a bug report was submitted on the Discord, but no card has been made for it.

### Type

This allows a slot filler to pretend to be a different type of property to a slot. This means that when determining which properties can be used to fill a slot, the slot filler will be permitted if this field matches the slot's type field instead of if the slot's type field is set to slot filler.

### Quantity \(Required\)

How many properties this counts as. When added to a slot, the slot filler will take up an amount of space in the slot equal to this value instead of simply 1. This will accept any non-negative number.

### Condition

A condition to check if you can add this slot filler to a slot. Unless you are making a library, this can be left blank. For this slot filler to be added to a slot, this condition must evaluate to true.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the slot.

### picture\*

The URL in the image field of the property.

### description\*

The text in the description field of the text, unparsed.

### slotFillerType\*

This returns the type of property this property counts as for filling a slot. The returned string will be the same as what would be used for an ancestor reference.

### slotQuantityFilled\*

This returns the number in the quantity field.

### slotFillerCondition\*

This returns the string in the condition field.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

