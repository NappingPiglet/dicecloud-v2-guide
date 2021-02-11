# Built-in Variables

Dicecloud V2 has some built-in variables available by default. This page is a listing of all currently available built-in variables.

Some variables listed here are only available in certain contexts. These variables will have an additional line in their description which states the context in which they're available for use.

{% hint style="info" %}
You can override any built-in variable by adding your own attribute with the same name! Do keep in mind that this isn't recommended in most situations, since it may interfere with some default functionality if done improperly.
{% endhint %}

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
      <td style="text-align:left"><code>level</code>
      </td>
      <td style="text-align:left">Your character&apos;s total level in all classes.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>milestoneLevels</code>
      </td>
      <td style="text-align:left">The number of milestone levels your character has.</td>
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
      <td style="text-align:left"><code>weightCarried</code> *</td>
      <td style="text-align:left">The current weight of all carried items.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>xp</code>
      </td>
      <td style="text-align:left">The amount of experience points your character has.</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
The `xp` and `milestoneLevels` variables reflect the events created in the [Experience view](../creating-your-first-character/the-character-tab.md#levels) on the Character tab, and are intended for determining when a character is ready to level up. Calculations for most actual character functionality should be based on `level` or `<class>.level` instead.
{% endhint %}

{% hint style="warning" %}
`allChecks`, `allSaves`, and `attackRolls` are present in Dicecloud's code, but do not currently function.
{% endhint %}

{% hint style="warning" %}
`weightCarried` is present and accessible, but is not currently calculated, and will always have a value of `0`.
{% endhint %}

