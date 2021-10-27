# Basic Library Conventions

When creating a library, there are certain conventions that should generally be followed. This page provides a list of some of these conventions, whether built into the system itself or recommended by the community.

## Attribute/Tag Listings and READMEs

It's recommended to include a note called README at the top level of your library, especially for larger libraries, with links, instructions, and other information on the library itself. Larger libraries should include sections or child notes with a list of all variable and tag names used in the library, to aid others in developing libraries that interact with theirs.

![An example README with attached attribute and tag lists.](/dicecloud-v2-guide/assets/library-readme-structure.png)

## Base Folders

In order for your custom base to work with the built-in Base slot that is created automatically for new characters, you'll need to tag the parent folder or slot filler for your base with the `base` tag.

![The tags field for the Kat's Core parent folder.](/dicecloud-v2-guide/assets/base-tags.png)

## Base Compatibility Tags

When creating properties meant to be used with slots, it's recommended to tag your properties with the names of whatever bases they're designed to be compatible with, for example `Kat's Core`. This allows those bases to filter out properties that don't work with their variable naming conventions, etc.

Below is a list of known compatibility tags for various libraries. Note that this is not necessarily an exhaustive list, and only reflects compatibility tags for libraries shared in the Dicecloud Discord server.

| Library                                                                                 | Compatibility Tag    |
| --------------------------------------------------------------------------------------- | -------------------- |
| [Devkit](https://beta.dicecloud.com/library/zE7NkWeJ6zvFYTiie)                          | `devkit`             |
| [Dicecloud 5e SRD](https://beta.dicecloud.com/library/qkv8aptJH2fCXARcJ)                | `5e`                 |
| [Jon's Spell Slot Structure](https://beta.dicecloud.com/library/2wuq3G9FM9bJ4sdsu)      | `jsss`               |
| [Obediah's Bag of Slot Fillers](https://beta.dicecloud.com/library/8weFtT657czESN8bc)   | `OBoSF`              |
| [Owlbear Essentials](https://beta.dicecloud.com/library/cBiPuuN2wbrBp2tbg)              | `OwlBE`              |
| [Tameran's Library of Everything](https://beta.dicecloud.com/library/hYPp44b6DvkgZkL2o) | `TLoE`               |
| [Langston and Jon's Races](https://beta.dicecloud.com/library/nAX82dWJvjYaqRiQf)        | `LJR`                |
| [Langston's Backpacks](https://beta.dicecloud.com/library/zH9DBYk2PWCACCany)            | `langstonsBackpacks` |
| [Khourdaet's Forge of Relics](https://beta.dicecloud.com/library/6zSDbwmiQvfccRWdw)     | `KFoR`               |

## Install Flags

Large libraries like bases are recommended to include a constant set to `true` in their core folder that other libraries can use to check if that library is present. Alternatively, you can set the constant to the library's version number, which will function the same thanks to truthy values, but also allow other libraries to check your library's version.

Below is a list of known install flags for various libraries. Note that this is not necessarily an exhaustive list, and only reflects install flags for libraries shared in the Dicecloud Discord server. Libraries which use the version number convention are noted in the right-hand column.

| Library                                                                                 | Install Flag                        | Uses Version # |
| --------------------------------------------------------------------------------------- | ----------------------------------- | -------------- |
| [Devkit](https://beta.dicecloud.com/library/zE7NkWeJ6zvFYTiie)                          | `devkit_installed`                  | No             |
| [Jon's Spell Slot Structure](https://beta.dicecloud.com/library/2wuq3G9FM9bJ4sdsu)      | `jsssInstalled`                     | No             |
| [Link the Balrog's Base](https://beta.dicecloud.com/library/NMgBJwmFKjkxvM8HW)          | `balrogBaseInstalled`               | No             |
| [Owlbear Essentials](https://beta.dicecloud.com/library/cBiPuuN2wbrBp2tbg)              | `owlbeInstalled`                    | Yes            |
| [Owlbear Extensions](https://beta.dicecloud.com/library/mZjyNMxYNNaHRgpA2)              | Various (all prefixed `owlbe_ext_`) | Yes            |
| [Tameran's Library of Everything](https://beta.dicecloud.com/library/hYPp44b6DvkgZkL2o) | `TLoEInstalled`                     | No             |

## Minimal Inclusion

When creating a library, especially a base, you should include as little as possible in your core folder. Wherever reasonable, include slots in the core and put pieces that aren't globally needed in slot fillers instead. This keeps the size of a given character sheet to an absolute minimum, which will help with performance when using your library.

A folder named something like "Internal" is recommended for larger libraries to separate your fillers, etc. from your core folder itself.

![An example Internal folder from Kat's Core, with subfolders for different types of fillers.](/dicecloud-v2-guide/assets/library-internal.png)
