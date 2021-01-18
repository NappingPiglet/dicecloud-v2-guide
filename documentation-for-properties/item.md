# Item

An item represents an object in your character's possession, whether magical or mundane.

## Components

### Icon

Select an icon to represent this item on the inventory page. Icons come from [game-icons.net](https://game-icons.net) and will change their color to match the item's color.

### Equipped

Is this item currently being worn or otherwise in a position from which it can be immediatly used? If this is false, then the item must be equipped before any of its children become active.

### Name

The name of the item, which will appear on the inventory tab when you only have one of the item.

### Plural Name

The name of the item for when you have multiple of it. It will be displayed on the inventory tab next to the quantity of the item. If this is left blank and you have more than one of the item, the singular name will be used.

### Value

The cost of the item in GP. Accepts numbers only. Currently serves no purpose, but this will change in later updates.

### Weight

The wieght of the container in pounds. Only accepts numbers. Currently serves no purpose, but this will change in later updates.

### Quantity \(Required\)

The number of the item you have. Accepts only numbers. This does not change how many times the item's children are applied, it only affects the cost and weight that are displayed when the item is selected in the inventory tab at present.

### Description

A description of the item, which will appear when you click on the item's name on the inventory tab. This field accepts markdown, HTML, and calculations within {}.

## Advanced

### Tags

Tags used to control which slots this property can be added to. Tags for items have a unique property in that they are also used for ammo tracking, allowing you to consume an item when performing an action.

### Show Increment Button

When set to true, an abacus button will appear next to the item name in the inventory tab. Clicking this will allow you to change the quantity of the item using the same UI as a health bar.

### Requires Attunment

Does this item need to be attuned to? Currently has no functionality beyond revealing the attuned slider.

#### Attuned

Are you currently attuned to the item? Currently has no functionality.
