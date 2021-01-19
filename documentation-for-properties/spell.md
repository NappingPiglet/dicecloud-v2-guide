# Spell

A spell is a magical effect that wizards, clerics and other casters can produce. These will usually be the children of [spell lists](spelllist.md) but do not have to be. If they are not, they will appear as a card on the spells tab.

## Components

### Always Prepared

If this is set to true, the spell is always able to be cast and will not contribute towards the maximum spells prepared of the spell list it is a child of.

### Prepared

If this is set to true, the spell will be visible on the spell list and can be cast. If it is false, you will only see it when changing your prepared spells, where you can make it prepared instead, and cannot cast it.

### Name

The name of the spell, which will appear on the spells tab.

### Level \(Required\)

The level of the spell, which determines what level of spell slot is the minimum that can be used to cast it. This exists on a scale of 0-9, with level 0 spells being called cantrips.

### School \(Required\)

The school of magic this spell belongs to.

### Casting Time

How long the spell takes to cast.

### Range

How far away from the caster the spell is capable of acting.

### Spell Components

What do you have to be able to in order to cast the spell? You can select as many or as few as you need.

* Verbal: Speaking is required for the spell.
* Somatic: You must be able to move your hands to cast the spell.
* Concentration: You must maintain concentration for the spell's effect to remain.
* Ritual: You may cast the spell without using a spell slot by adding 10 minutes to the casting time.

### Material

What material components, if any, are required to cast this spell. Most classes allow you to use a focus of some variety if the material components do not have a gold cost.

### Duration

How long the spell's effect remains. If it says "up to x", then you may end the effect as a free action and usually must maintain concentration.

### Description

A long description of the spell, which will appear when you click on the feature's name on the spells tab. This field accepts markdown, HTML, and calculations within {}.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Casting

This section is identical to the [action](action.md) property, with the only difference being that the description will match the text in the description field above. When you set an icon in this section, it will appear with the spell name on the spell list and on the list of castable spells. After you cast a spell from the stats page, children of the spell will be carried out as if you had taken an action.
