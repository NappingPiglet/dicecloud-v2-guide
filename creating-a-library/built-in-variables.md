# Built-in Variables

Dicecloud V2 has some built-in variables available by default. This page is a listing of all currently available built-in variables.

Some variables listed here are only available in certain contexts. These variables will have an additional line in their description which states the context in which they're available for use.

<p class="hint info">
You can override any built-in variable by adding your own attribute with the same name! Do keep in mind that this isn't recommended in most situations, since it may interfere with some default functionality if done improperly.
</p>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Variable Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>allChecks</code> *</td>
      <td style="text-align:left">Target for proficiencies to give proficiency in all checks.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>allSaves</code> *</td>
      <td style="text-align:left">Target for proficiencies to give proficiency in all saving throws.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>attackRolls</code> *</td>
      <td style="text-align:left">Target for bonuses to all attack to-hit rolls.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>attackRoll</code>
      </td>
      <td style="text-align:left">
        <p>The roll, without modifiers, of the attack this property is a child of.</p>
        <p><em>Context: attack/spell children during execution</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>criticalHit</code>
      </td>
      <td style="text-align:left">
        <p><code>true</code> if the attack is a critical hit (<code>attackRoll &gt;= criticalHitTarget</code>)</p>
        <p><em>Context: attack/spell children during execution</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>criticalHitTarget</code>
      </td>
      <td style="text-align:left">The minimum dice roll needed to land a critical hit, <code>20</code> by
        default.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>itemsAttuned</code>
      </td>
      <td style="text-align:left">The number of items you are currently attuned to.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>level</code>
      </td>
      <td style="text-align:left">The character&apos;s total level in all classes.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>milestoneLevels</code>
      </td>
      <td style="text-align:left">The number of milestone levels your character has.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>proficiencyBonus</code>*</td>
      <td style="text-align:left">The character&apos;s proficiency bonus.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>savingThrow</code>
      </td>
      <td style="text-align:left">
        <p>The roll, with modifiers, of the saving throw this property is a child
          of.</p>
        <p><em>Context: saving throw children during action execution</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>savingThrowRoll</code>
      </td>
      <td style="text-align:left">
        <p>The roll, without modifiers, of the saving throw this property is a child
          of.</p>
        <p><em>Context: saving throw children during action execution</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>slotLevel</code>
      </td>
      <td style="text-align:left">
        <p>The spell slot level currently being cast with.</p>
        <p><em>Context: spell children during casting</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>toHit</code>
      </td>
      <td style="text-align:left">
        <p>The roll, with modifiers, of the attack this property is a child of.</p>
        <p><em>Context: attack/spell children during execution</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>valueCarried</code>
      </td>
      <td style="text-align:left">The value of all items in the inventory, except items in containers with
        &quot;Carried&quot; turned off.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>valueEquipment</code>
      </td>
      <td style="text-align:left">The value of all equipped items.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>valueTotal</code>
      </td>
      <td style="text-align:left">The value of all items in the inventory.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>weightCarried</code>
      </td>
      <td style="text-align:left">The weight of all items in the inventory, except items in containers with
        &quot;Carried&quot; turned off or &quot;Contents are weightless&quot; turned
        on.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>weightEquipment</code>
      </td>
      <td style="text-align:left">The weight of all equipped items.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>weightTotal</code>
      </td>
      <td style="text-align:left">The weight of all items in the inventory.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>xp</code>
      </td>
      <td style="text-align:left">The amount of experience points your character has.</td>
    </tr>
  </tbody>
</table>

<p class="hint info">
The `xp` and `milestoneLevels` variables reflect the events created in the [Experience view](../creating-your-first-character/the-character-tab.md#levels) on the Character tab, and are intended for determining when a character is ready to level up. Calculations for most actual character functionality should be based on `level` or `<class>.level` instead.
</p>

<p class="hint info">
All `value` and `weight` properties include container values/weights in their calculations.
</p>

<p class="hint info">
`weightCarried` includes containers with "Contents are weightless" turned on, but not their items. It does not include containers or their items if "Carried" is turned off.
</p>

<p class="hint warning">
`allChecks`, `allSaves`, and `attackRolls` are present in Dicecloud's code, but do not currently function.
</p>

<p class="hint warning">
`proficiencyBonus` is added by default to attack bonus calculations on property creation, and automatically calculated for application to skill proficiencies. However, it is not accessible anywhere else, and will need to be created and managed by a base to be accessible in any other context.
</p>

