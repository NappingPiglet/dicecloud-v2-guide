# Character Creation 101

Dicecloud is an immensely powerful and flexible character management app, and as such its learning curve is quite steep. However, if you just want to create a simple character and get playing as fast as possible, this guide is for you.

This section of the guide assumes that you are playing Dungeons and Dragons Fifth Edition, 5e for short. The same basic principles apply for other systems, but the examples given will be as such.

## Selecting a Base

The first thing you'll need to do when creating a new character is choose your base - in other words, an implementation of the core rules and stats of whatever game system your character is designed for. While it's quite possible to create your own, this is a lot of unnecessary work, and avoiding this type of work is the purpose of libraries.

These are currently the most prominent bases for 5e:

* [Dicecloud 5e SRD](https://beta.dicecloud.com/library/qkv8aptJH2fCXARcJ) by Thaum Rystra
  * Currently WIP, but will eventually become Dicecloud's "built-in" default, which everyone will automatically be subscribed to.
* [Link the Balrog's Base](https://beta.dicecloud.com/library/NMgBJwmFKjkxvM8HW) by LinkTheBalrog
  * Provides a simple, no-nonsense set of basic stats and so on. Only contains the basics and will need to be augmented with other libraries for races, classes, etc.
* [Kat's Core](https://beta.dicecloud.com/library/dGb2n9TEheo3PnAZa) by KatrinaKitten
  * Provides a more heavily-automated experience, with most materials like races, classes, etc. self contained within one library.

Once you've subscribed to the library for the base of your choice, you can create your character! Head to the Characters tab in the sidebar, and hit the + button at the bottom right. You'll be taken to the Character tab, with the Build view open - it should look something like this.

![The Build view shown when you first create a character.](../.gitbook/assets/image%20%283%29.png)

## The Slot System

Now that you're in the Build view, you should see a + button under the heading "Base". This is the slot interface, and is the primary way of making decisions about your character in V2.

A slot is, in essence, a hole in your character sheet, which can be filled with various options. Assuming your base of choice is set up well, you should be able to do most of your character creation process just by hitting the + button below a given slot's label, selecting an option from the menu that pops up, and clicking "Insert" at the bottom right.

Selecting which base to use for a given character is just as simple as making further decisions via slots; just hit the + button, select your base, and hit Insert. From there, you're good to go!

{% hint style="info" %}
Slots are primarily a library creation utility. The options they pull in aren't actually in your sheet until you click "Insert"; rather, they're stored in whatever libraries you've subscribed to. You should almost never need to create a slot in your own sheet manually.
{% endhint %}

Once you've made your selections to create your character, you can switch to the Stats, Features, Inventory, and Spells tabs to see the result.

## The Dice Roller

When you first open a character sheet, you'll see an empty right-hand sidebar with a text field at the bottom. This is the dice roller, and it serves as an output log for the results of your character's actions. You can enter any [expression](../creating-a-library/parser-documentation.md) in the text field at the bottom to calculate it, and things like damage rolls from your actions and attacks will be automatically displayed here.

You can show or hide the dice roller by clicking the three lines at the top right of the character sheet.

