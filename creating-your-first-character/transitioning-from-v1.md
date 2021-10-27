# Transitioning from V1

If you've used Dicecloud V1, V2 can be used in a very similar fashion, but there are certain differences you'll need to get used to. If you're not using homebrew materials, chances are that either the [default SRD library or a community-made library](character-creation-101.md#selecting-a-base) has what you need via the [Build card on the Character tab](the-character-tab.md#build); if you really need to make your own, though, this page lists the low-level core changes you should be aware of.

### Formulas

| Name                    | V1 syntax                        | V2 syntax                          |
| ----------------------- | -------------------------------- | ---------------------------------- |
| Ability Score Modifiers | `strengthMod`                    | `strength.modifier`                |
| Class Levels            | `FighterLevel`                   | `fighter.level`                    |
| Conditionals            | `if(condition, ifTrue, ifFalse)` | `condition ? ifTrue : ifFalse`     |
| Spell Attack Bonus      | `attackBonus`                    | `#spellList.attackRollBonusResult` |
| Spell DC                | `DC`                             | `#spellList.dcResult`              |
