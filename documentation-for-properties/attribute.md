# Attributes

An attribute adds a variable to the character sheet. Common attributes include things such as AC, ability scores and spell slots.

## Components

### Base Value

The base value is the starting value of the attribute. This can be either a number or a calculation. If you apply a second base value later, such as from an effect component, the highest base value will be used.

### Name

The name of the attribute. This will appear on the stats page alongside the attribute's current value.

### Variable Name \(Required\)

The name of the attribute used to identify it in calculations or other components. This will both uppercase and lowercase latin characters, numbers and underscores, but will not accept characters such as spaces.

### Type \(Required\)

The type of the attribute. This is a dropdown, used to be more specific about the purpose of the attribute, as well as control where on the stats page it appears.

* Ability Score
  * A stat such as strength, dexterity or constitution. These appear on your stats page alongside a modifier \(which is calculated as the attribute's current value, minus 10, divided by 2 and then rounded down\).
* Stat
  * A stat used to track a value such as armor class, speed or darkvision range. These appear on your stats page and are the default value of the type field.
* Modifier
  * A modifier is used to track a value that will be added or subtracted from rolls or other calculations. These include things such as proficiency bonus and initiative. They will appear on your stats page alongside either a plus or minus sign, depending on if the value is positive or negative.
* Hit Dice
  * A hit dice is used to restore hit points during a short rest. The base value field controls how many of this type of hit dice you have, and they appear on the stats page as the current value slash the max value, with an increment button to one side and the hit dice size on the other side, which will be followed by `+ constitution.modifier`.
    * **Hit Dice Size**
      * An additional field that only appears for hit dice type attributes, this allows you to select what the dice size of the hit dice is. Your options are d20, d12, d10, d8, d6 and d4.
* Health Bar
  * A health bar appears at the top of your stats page and is used to track values on a sliding bar. When damage is applied to a character using an action, it will be applied to the lowest health bar, as will healing.
* Resource
  * A resource is used to track the uses of an ability or a value like ki that you expend to fuel powers. These appear on the stats page in the same way as hit dice, but with the attribute name instead of the dice size.
* Spell Slot
  * A spell slot is used by the spellcasting classes of D&D to fuel their magic. These appear on the stats page as a series of bubbles that are either empty or filled, with the name of the attribute next to them.
    * **Spell Slot Type**
      * An additional field that only appears for spell slot type attributes, this allows you to specify the level the spell slot. This can be either a number or a calculation and currently has no use, though a spellcasting update is planned for the future.
* Utility
  * A utility is used to track a value that is normally hidden, such as whether a certain feature has been taken or your spellcaster level. These don't appear on the stats page.

### Description

The description of the attribute. This field accepts markdown, HTML, and calculations within {}. This will appear when you click on the property, whether from the stats page or from another property.

## Advanced Components

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

### Allow Decimal Values

Allows the attribute to store a decimal as a value. When set to false, decimals will be rounded to the nearest down.

### Damage

This field cannot be interacted with.

### Reset

This controls when the property is restored to its max value. The options are short rest and long rest. If you choose short rest, it will also regain its max value on a long rest. Rests can be triggered from the stats page.

## Accessible Values

### attributeType

Returns the type of the attribute, given in the type field.

### name

Returns the name of the attribute, given in the name field. If the field has not been filled out, returns the text `<attributeName>.name`.

### reset

Returns longRest if the attribute's reset field is set to a long rest and returns shortRest if it is set to short rest. If the field has not been filled out, returns the text `<attributeName>.reset`.

### decimal

Returns true if the attribute can have a decimal point for it's value. Returns `<attributeName>.decimal` otherwise.

### damage

Returns the current attribute damage the attribute is suffering from. If this value is 0, returns `<attributeName>.damage`.

### currentValue

The current value of the attribute, with attribute damage and all calculations applied.

### value

Returns the current value of the attribute without attribute damage.

### modifier

The modifier of the value. This only exists for ability score type attributes and is calculated as `floor((attributeName-10)/2)`.

### baseValue

The value of the attribute without any modifiers.

### spellSlotLevelValue

Returns the level of the spell slot this attribute represents if the attribute type is spell slot. Otherwise returns `<attributeName>.spellSlotLevelValue`.

<<<<<<< HEAD
## Hidden Values

Note that the following values can only be accessed by using the `#attribute.<valueName>` syntax from a child of the attribute.

### description

Returns the description of the attribute

### baseValueCalculation

Returns the text entered into the base value field, unparsed.

### spellSlotLevelCalculation

Returns the text entered into the slot level field, unparsed. If the attribute is not a spell slot type, it instead returns `#attribute.spellSlotLevelCalculation`.

### constitutionMod

Returns the modifier for the constition attribute. This can only be accessed if the attribute is of type hit dice. This does not return a value with any relation to this particular attribute, but instead equivalent to putting `constitution.modifier`.
=======
>>>>>>> c47eaf342d6d896d35a75da11b5a1c56f04c79c9
