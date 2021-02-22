# Actions

An action is used to indicate something that your character does, such as swinging a sword or drinking a potion.

## Components

### Icon

Select an icon to represent this action on the stats page. Icons come from [game-icons.net](https://game-icons.net) and will change their color to match the action's color.

### Name

The name of the action, which will appear on the action's card on the stats page.

### Action Type \(Required\)

The type of the action, which represents how much time or effort it takes to perform the action.

* Action
  * A standard action, the default used for tasks during gameplay.
* Bonus Action
  * A bonus action is less time intensive than a standard action, and is commonly used to represent performing a task that is either low effort or that you have trained to do in a very brief time.
* Attack Action
  * Unlike in normal D&D 5e, in DiceCloud an attack action represents one of the attacks you make when you attack on your turn. In most cases, you will want to use the [Attack](attack-action.md) property instead.
* Reaction
  * A reaction is something you can do when it isn't your turn in response to something else happening. Common examples include using a spell such as _Shield_ or responding after taking the ready action.
* Free Action
  * A free action is something like talking or activating an ability that doesn't require an action of any sort. The number of times you can take a given free action per round depends on the specific action.
* Long Action
  * A long action is something that takes multiple rounds to accomplish, such as casting certain spells.

### Summary

A brief summary of the action, which will appear beneath the name of the action on the stats tab. This field accepts markdown, HTML, and calculations within {}.

### Description

A long description of the action, which will appear when you click on the action's name or summary on the stats tab. This field accepts markdown, HTML, and calculations within {}.

## Resources

Resources are a method of consuming either an item or an attribute during the usage of an action.

* Attribute
  * This consumes a quantity of an attribute when you use the action.
    * Note: You can pass an attribute that has no reset property, but if you do so the attribute will never be restored, so it is usually not wise to do so.
* Ammo
  * This consumes a quantity of an item that has the tag you give the tags field. You will be prompted to select an item as ammo on the stats page before you can take the action.

## Advanced

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

### Target

Whether the action will affect you, one other creature or multiple creatures. Has no functionality at the moment.

### Uses

How many times you can use this ability before needing to rest. Accepts either a number or a calculation.

### Uses Used

How many times you have used this ability since it was last restored. If you have a limited number of uses, you should input either a 0 or some starting value for this field to avoid being told the action has NaN uses remaining.

### Reset

This controls when the property is restored to its max value. The options are short rest and long rest. If you choose short rest, it will also regain its max value on a long rest. Rests can be triggered from the stats page.

## Accessible Values

### name\*

The name of the action.

### description\*

Returns the description of the action.

### summary\*

Returns the summary of the action.

### actionType\*

Returns what the action has is the action type field.

### target\*

Returns what has been selected in the target field under advanced, in camelCase.

### uses\*

Returns the number of uses the action has at max.

### usesUsed\*

Returns the number of times this action has been used since the uses were last reset.

### reset\*

Returns the type of rest need for the action's uses to reset, in camelCase.

### usesResult\*

Returns the number of times you can use the action before one resource, ammo or uses remaining is insufficient.

### insufficientResources\*

Returns true if the action cannot be taken because the resources consumed aren't satisfied. If no resources are consumed, returns `#action.insufficientResources`.

{% hint style="warning" %}
All values marked with \* can only be accessed using an ancestor reference.
{% endhint %}

