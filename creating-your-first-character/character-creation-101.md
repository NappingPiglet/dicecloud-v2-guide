# Character Creation 101

Dicecloud is an immensely powerful and flexible character management app, and as such its learning curve is quite steep. However, if you just want to create a simple character and get playing as fast as possible, this guide is for you.

This section of the guide assumes that you are playing Dungeons and Dragons Fifth Edition, 5e for short. The same basic principles apply for other systems, but the examples given will be as such.

The first think you do when creating a new character is give it a Name.  You can also set alignment, gender, images.

![image](https://user-images.githubusercontent.com/93097663/139508825-f6914898-329f-491d-ab22-e0e6cd2a396d.png)


and additonal settings

![image](https://user-images.githubusercontent.com/93097663/139508857-eb400e86-802f-45c5-9bee-ac922ddf8630.png)

You will be directed to the build card in the Character view, which will appear empty

![image](https://user-images.githubusercontent.com/93097663/139509094-e2a07eb9-d1a8-4020-bf86-61216d83c6ab.png)


## Selecting a Different Ruleset (previously called base)

A ruleset is an implementation of the core rules and stats of whatever game system your character is designed for. While it's quite possible to create your own, this is a lot of unnecessary work, and avoiding this type of work is the purpose of libraries.

The default ruleset is

* [Dicecloud 5e SRD](https://beta.dicecloud.com/library/qkv8aptJH2fCXARcJ) by Thaum Rystra
  * Currently WIP, but will eventually become Dicecloud's "built-in" default, which everyone will automatically be subscribed to.
  * This rules might interfere with other base libararies like TLoE.  You can remove it when adding new Rulesets.

These are currently the most prominent rules for 5e:

* [Link the Balrog's Base](https://beta.dicecloud.com/library/NMgBJwmFKjkxvM8HW) by LinkTheBalrog
  * Provides a simple, no-nonsense set of stats and so on. Contains a large infastructure, laying the groundwork for libraries to be built off of, but will need to be augmented with other libraries for races, classes, etc. It should be noted that this library was created in the early days of V2, and as such does not make use of various features, such as slots or references.
* [Tameran's Library of Everything](https://beta.dicecloud.com/library/hYPp44b6DvkgZkL2o) by Jonpot
  * Currently the most complete base ruleset in terms of content, this library is structured to use multiple sub-libraries in order to store all of its content. TLoE itself provides classes and backgrounds as well as the character base.
  * [Obediah's Bag of Slot Fillers](https://beta.dicecloud.com/library/8weFtT657czESN8bc) by Jonpot is the primary sub-library for TLoE, containing slot fillers used across all the other rulesets, such as proficiencies, spells, and feats.
  * [Langston & Jon's Races](https://beta.dicecloud.com/library/nAX82dWJvjYaqRiQf) by Langston_Hughes and Jonpot is the race sub-library for TLoE, containing the various published races for D\&D 5e.
  * [Khourdaet's Forge of Relics](https://beta.dicecloud.com/library/6zSDbwmiQvfccRWdw) by Ganonslayer is the primary item library for TLoE, containing weapons and armor, as well as adventuring gear and spell components. Currently contains very few magic items, but if a specific item is needed, one can contact Ganonslayer#4106 on Discord to see about having it added.
  * [Arianna's Tome of Beasts](https://beta.dicecloud.com/library/EDBGcBPh2xsEvTvfh) by Jonpot is a library containing wildshape slot fillers for duids. Currently far from complete.
  * [Jon's Spell Slot Structure](https://beta.dicecloud.com/library/2wuq3G9FM9bJ4sdsu) by Jonpot is the spellcasting library for TLoE, providing spell slots for the various spellcasting classes.
* [Owlbear Essentials](https://beta.dicecloud.com/library/cBiPuuN2wbrBp2tbg) by KatrinaKitten
  * Just the (Owl)bare essentials. Primarily serves as a more up-to-date alternative to Link's base, by supporting features like slots and constants.

Once you've subscribed to the library for the Ruleset of your choice, you can create your character! Head to the Characters tab in the sidebar, and hit the + button at the bottom right. You'll be taken to the Character tab, with the Build view open, like the picture above.

You can change the Ruleset to your subscribed choice by clicking on the "Build" title bar and you should see this:

![image](https://user-images.githubusercontent.com/93097663/139509328-25497976-abd4-46a4-94c2-021ad07e33ec.png)

From there you can delete the 5e default and add your ruleset as the "base."

![image](https://user-images.githubusercontent.com/93097663/139509523-4c2e2cdb-262e-4364-80f8-0d7480ec510d.png)

Click on the checkbox for your ruleset and then the red "1/1 Insert" and the the card will update:

![image](https://user-images.githubusercontent.com/93097663/139509624-6c00e6a3-26ed-4c9f-bef2-90822c18531c.png)


## The Slot System

Now that you're in the Build view, you should see a + button under the heading Race. This is the slot interface, and is the primary way of making decisions about your character in V2.

A slot is, in essence, a hole in your character sheet, which can be filled with various options. Assuming your ruleset of choice is set up well, you should be able to do most of your character creation process just by hitting the + button below a given slot's label, selecting an option from the menu that pops up, and clicking "Insert" at the bottom right.

{% hint style="info" %}
Slots are primarily a library creation utility. The options they pull in aren't actually in your sheet until you click "Insert"; rather, they're stored in whatever libraries you've subscribed to. You should almost never need to create a slot in your own sheet manually.
{% endhint %}

Once you've made your selections to create your character, you can switch to the Stats, Features, Inventory, and Spells tabs to see the result.

## The Dice Roller

When you first open a character sheet, you'll see an empty right-hand sidebar with a text field at the bottom. This is the dice roller, and it serves as an output log for the results of your character's actions. You can enter any [expression](../creating-a-library/parser-documentation.md) in the text field at the bottom to calculate it, and things like damage rolls from your actions and attacks will be automatically displayed here.

You can show or hide the dice roller by clicking the three lines at the top right of the character sheet.
