# Skills

A skill is used to track your ability to perform a task, such as hiding from an enemy or running a marathon. They appear on the stats page, in columns separated by skill type.

## Components

### Name

The name of the skill, which appears on the stats page to the right of a circle which indicates the level of proficiency you possess.

### Variable Name \(Required\)

The name of the skill's variable, which will be used to access the skill for calculations and effects. Accepts both uppercase and lowercase Latin characters, number, and underscores. Spaces are not accepted.

### Ability

The ability score that is used to determine the base bonus you receive when making checks with this skill. The bonus will only appear if a value is given for this field, and will appear to the left of the skill's name on the stats page. Only attributes who's type is ability score can be used for this field.

### Type \(Required\)

The type of skill this is.

* Skill
  * A normal skill, such as stealth or athletics, commonly used for normal checks and almost always with an associated ability score.
* Save
  * A saving throw, which is used to protect yourself from a harmful ability or measure your ability to use a certain ability defensively.
* Check
  * Each check type skill displays on its own card on the stats page instead of in a column with other skills of the same type.
* Tool
  * A tool proficiency represents your ability to use a tool to achieve a goal, such as picking a lock or crafting a sword.
* Weapon
  * A weapon proficiency represents your ability to use a weapon in combat, and allows you to add your proficiency bonus to attack rolls made with that weapon.
* Armor
  * An armor proficiency represents your ability to wear armor effectively or use a shield. Without proficiency, you suffer certain penalties when wearing armor and cannot cast spells while in the armor.
* Language
  * A language proficiency represents your ability to speak a language. Almost all characters have proficiency in at least one language.
* Utility
  * A utility skill is not displayed anywhere, and is used to track an invisible value such as adding your proficiency bonus to certain spells as an abjuration wizard.

### Description

A description of the purpose of the skill, which will display when the skill is clicked on. This field accepts Markdown, HTML, and calculations contained within {}.

## Advanced

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

### Base Value

An override to the bonus you have to checks using this skill before factoring in effects, the ability score or proficiency. By default is set to 0, but if you add a zero for this value the skill will appear even when hide redundant stats is set to true. This can be either a number or a calculation.

### Base Proficiency

The basic level of proficiency you have in a skill. By default, this is not proficient.

## Accessible Values

### name

Returns the name of the skill.

### variableName\*

The variable name of the skill.

### ability

Returns the name of the ability score given for the skill's ability field. If the field has not been filled out, returns the text `<skillName>.ability`.

### baseValueCalculation\*

Returns the string in the base value field, unparsed.

### baseProficiency

Returns the base proficiency of the skill, given in the base proficiency field. If the field has not been filled out, returns the text `<skillName>.baseProficiency`.

### description\*

Returns the description of the skill, unparsed.

### abilityMod

Returns the modifier of the ability score given for the skill's ability field. If the field has not been filled out, returns the text `<skillName>.abilityMod`.

### baseValue

Returns the value given for the base value field or given by an effect. If no such value exists, returns the text `<skillName>.baseValue`.

### proficiency

This returns the multiplier of your proficiency bonus for the skill. Passes 0 for not proficient, 0.5 for half proficiency, 1 for proficient and 2 for expertise.

### value

This returns the bonus you have when using this skill. Returns NaN if no such modifier exists.

### advantage

This returns a -1 for having disadvantage with the skill, 0 for having neither advantage or disadvantage, and 1 for having advantage.

### passiveBonus

This returns the bonus you have to passive checks using this skill. If you have a net 0 modifier to your passive bonus to the skill this returns 0.

### fail

This returns 1 if you automatically fail checks using this skill. Otherwise returns 1.

### conditionalBenefits

Should return an array containing all conditional benefits to the skill, but currently just throws an error and hides whatever text it is part of.

### rollBonuses

Should return an array containing all bonuses to rolls using to the skill, but currently just throws an error and hides whatever text it is part of.

### hide\*

Returns true if the skill is hidden for some reason.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

