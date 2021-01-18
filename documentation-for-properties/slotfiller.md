# Slot Filler

A slot filler is a property that is intended to allow for greater control over filling slots, and will usually have additional properties as children that grant features or other effects.

## Components

### Icon

Select an icon to represent this slot filler on the character page. Icons come from [game-icons.net](https://game-icons.net) and will change their color to match the slot filler's color.

### Name

The name of the slot filler, visible under the slot it is added to from the character page.

### Description

A description of the slot filler, which will appear when you click on the slot filler's name on the character tab. This field accepts markdown, HTML, and calculations within {}.

### Picture URL

A URL to an image to represent this slot filler, which will be visible when in the dialogue to add it to a slot. Currently bugged (?), a bug report was submitted on the Discord, but no card has been made for it.

### Type

This allows a slot filler to pretend to be a different type of property to a slot. This means that when determining which properties can be used to fill a slot, the slot filler will be permitted if this field matches the slot's type field instead of if the slot's type field is set to slot filler.

### Quantity \(Required\)

How many properties this counts as. When added to a slot, the slot filler will take up an amount of space in the slot equal to this value instead of simply 1. This will accept any non-negative number.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.
