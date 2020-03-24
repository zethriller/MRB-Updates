# Mids' Reborn Unofficial (MRBU)
### Current MRBU Version: _20.2604_

___Please note that all unofficial updates are based off of City of Heroes: Homecoming and may not reflect other City of Heroes server implementations.___

@Zed (Discord: Zed#7901)  
@Felis Noctu (Discord: Feles Noctis#9086)  
@Procat (Discord: Procat#3599)  
Metalios (Discord: Metalios#2673)

---
---
---

# Install Instructions
* Above right, find and click the green button labeled __"Clone or Download"__
* Click __"Download ZIP"__
* Open downloaded file
* Extract contents of __"MRB-Updates-master"__ to Mids install folder, overwriting as prompted
  * _For a clean install, only extract the __"Data"__ and __"Images"__ folders_

---
---
---

# 2.6.0.7 I26P4
_(as of 2020-03-23)_

## __MRBU Features__
### Database Version Number
* As of this Issue/Page number, the Mids database version is going to be formatted to match the date of the last update, in order to make comparing versions at a glance easier for both devs and players.
  * __Year:__ 2020  
  __HC Vers:__ Issue 26, Page 4  
  __DB Date:__ 23/03/2020  
  __DB Vers:__ 20.2604

### Homecoming Beta Server Previews
* We’re in the process of adding Beta-specific content and changes to Mids’ to allow for analysis and number crunching of Homecoming’s beta changes. These sets may be found by looking for anything beginning with “z_”, which in the case of powersets will push them to the bottom of their respective lists.
* As the beta server is changing much more frequently than on live, and the beta BIN files are currently difficult to parse to extract raw data, this added content may not always be 100% accurate. We’ll do our best to get them as close as we can!

## __General Archetype Updates__
### Brute
* Fiery Aura powers updated to reflect current in-game values

### Corruptor
* Most primary specialization powers updated to reflect current in-game values
  * Does not include Snipe powers at this time
* Many Storm Summoning powers updated to reflect current in-game values

### Scrapper / Stalker
* Fix for Ancillary pool being locked when adding a snipe power
  * To accomplish this, Quick Form has been moved from ancillary pools to class inherent abilities - so it's always there even if you don't take any snipe power. This change might unlock your existing builds, but that hasn’t been tested.

## __Tanker & Brute Changes__
### AoEs, Scaling & Stats, and Others
* These changes are wide-reaching and difficult to manage from a purely database-editing angle. Mids’ does have AT class modifiers integrated, however they’re hardcoded and compiled as part of the program itself. As well, they’re massive lists of values that would need to be carefully adjusted based on what Homecoming currently uses, which would require being able to get a hold of that information. BIN parsing for the game files still isn’t at 100%, and as such we’re taking the more difficult path and updating each power’s values individually, a very slow process. As such some values may not match in-game numbers. This is an ongoing process.
  * Brute Primaries > Status unknown
  * Brute Secondaries > Status unknown
  * Tanker Primaries > WIP
  * Tanker Secondaries > WIP
    * Updated:
      * Battle Axe
      * Broad Sword
      * Claws
      * Dark Melee
      * Electrical Melee
      * Energy Melee

## __Powers__
### Powers Update & Fixes
* The following powers had their scaling resistance bonuses reimplemented:
  * Arachnos Widow > Teamwork > Foresight
  * Brute > Super Reflexes > Agile
  * Brute > Super Reflexes > Dodge
  * Brute > Super Reflexes > Lucky
  * Scrapper > Super Reflexes > Agile
  * Scrapper > Super Reflexes > Dodge
  * Scrapper > Super Reflexes > Lucky
  * Sentinel > Super Reflexes > Agile
  * Sentinel > Super Reflexes > Dodge
  * Sentinel > Super Reflexes > Enduring
  * Stalker > Super Reflexes > Agile
  * Stalker > Super Reflexes > Dodge
  * Tanker > Super Reflexes > Agile
  * Tanker > Super Reflexes > Dodge
  * Tanker > Super Reflexes > Lucky
* The following powers had their damage over time values corrected:
  * Corruptor > Beam Rifle > Lancer Shot
  * Corruptor > Fire Blast > Rain of Fire
  * Corruptor > Ice Blast > Blizzard
  * Corruptor > Ice Blast > Ice Storm
  * Corruptor > Storm Summoning > Freezing Rain
  * Corruptor > Water Blast > Whirlpool
* The following powers have been marked as a click-buff to allow toggling of the effect:
  * Blaster > Temporal Manipulation > Chronos
  * Dominator > Martial Assault > Envenomed Blades
  * Pools > Presence > Unrelenting
* Arachnos Widow > Fortunata Teamwork > Mind Link: Values adjusted
* Arachnos Widow > Widow Training > Follow Up: Damage and ToHit bonuses now scale
  * Damage: 30% per stack, up to 4 stacks (120%)
  * ToHit: 10% per stack, up to 4 stacks (40%)
* Arachnos Widow > Widow Teamwork > Mind Link: Various values adjusted
* Blaster > Atomic Manipulation > Beta Decay: Recharge bonus now scale correctly
  * 10% base + 2.5% per stack, up to 10 stacks (25%)
* Blaster > Plant Manipulation > Wild Fortress: Absorb value adjusted
* Blaster > Tactical Arrow > ESD Arrow
  * Endurance cost adjusted
  * Description updated
* Pools > Flight > Hover: Endurance cost adjusted
* Sentinel > Invulnerability > Durability: Absorb changed to MaxHP  
  _NOTE: In-game information claims MaxAbsorb, but power effects extracted from game files as of 2020-03-08 indicate MaxHP. This means it will not be enhanced by Cardiac Radial Alpha._
* Sentinel > Radiation Armor > Particle Shielding: Allowed slotting of EndMod enhancements

### Super Reflexes / Arachnos Widow Foresight
* SR’s original implementation was Scrapper-exclusive and relied on a flat, consistent, non-AT-modified, unenhanceable, unbuffable slope for its values as its passives’ resistances scaled up. When the set/effect was proliferated to other archetypes this slope was maintained with only minor adjustments to the base values.
  * Brute, Scrapper, and Tanker resistance begins building at 60% Max HP, reaching 20% resistance per passive at 0% Max HP
  * Sentinel/Stalker resistance begins building at 60% Max HP, reaching 25% res per passive at 0% Max HP
  * Arachnos Widow > Teamwork > Foresight resistance begins building at 75% Max HP, reaching 32.25% at 0% Max HP.  
  _NOTE: Game description states it gives slope resistance to all damage types, but like SR's passives Foresight does not actually include Psionic or Toxic resistance._

### Pools
* Sorcery and Force of Will are now mutually exclusive. In addition to a visual clue, there is a
  note about it in the powersets' descriptions.  
  _→ KNOWN ISSUE: Exclusivity is only shown when attempting to take powers from two sets._

### Incarnates
* Enabling a Diamagnetic Interface will no longer debuff the player's regeneration, resistances, or tohit
* Enabling a Reactive Interface will no longer debuff the player's resistances

### IO Sets
* Sudden Acceleration: Knockback to Knockdown 
  * This set will now only affect the power it is slotted in, as in-game.

## __Powers (HC beta)__
### New Support Powerset: Electrical Affinity
* __Label:__ z_Electrical Affinity  
  _Up to date as of I26p5 Build 4_
* Currently only implemented for Defenders  
  _→ KNOWN ISSUE: Mids does not currently appear to be able to display Targeted Absorbs, so Insulating Circuit will show as (Self)._

### New Origin Power Pool: Experimentation
* __Label:__ z_Experimentation  
  _Up to date as of I26p5 Build 4_
* Added powerset icon
* Added scales and modifiers so it has variance among ATs
* Experimentation > Corrosive Vial:
  * Effects now use pseudo-pet

### Power Updates & Fixes
* The following Leadership _(z_Leadership)_ powers have had their activation time reduced from 3.63 seconds to 1.5 seconds
  * Pools > Leadership > Maneuvers
  * Pools > Leadership > Assault
  * Pools > Leadership > Tactics

### Pools
* Experimentation, Sorcery, and Force of Will are now mutually exclusive. In addition to a visual
  clue, there is a note about it in the powersets' descriptions.  
  _→ KNOWN ISSUE: Exclusivity is only shown when attempting to take powers from two sets._

### IO Sets
* NEW (up to date as of I26p5 Build 3)
  * Artillery (Targeted AoE, Rare, 30-50)
  * Bombardment (Targeted AoE, Rare, 30-50)
  * Preemptive Optimization (Endurance Modification, Uncommon, 21-50)
  * Power Transfer (Endurance Modification, Rare, 21-50)
  * Synapse’s Shock (Endurance Modification, Rare, 21-50)

## __To-Do__
### General
* Snipe powers may be missing data
* Water Jet may be missing some data

### Power Updates & Fixes
* Dominator > Martial Assault > Envenomed Blades: Correct power not adding toxic damage to other attacks
* Pools > Force of Will > Weaken Resolve: Reenable slotting of Accurate ToHit Debuff enhancement sets
* Scrapper > Titan Weapons > Defensive Sweep: Correct defense bonus to in-game value of 11.25%

## __Known Issues__
### Need More Information
* Water Jet damage value for Blasters doesn’t match in-game.  
  _→ Will need to investigate calculation differences_

### Can’t/Won’t Fix
* ATOs and Superior ATOs are not marked as mutually exclusive.  
  _→ Won't fix. Not related to database, and would require extensive Mids’ code changes to accomplish._
