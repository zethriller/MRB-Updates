# Mids' Reborn Unofficial (MRBU)
### Current MRBU Version: _20.2605_

___Please note that all unofficial updates are based off of City of Heroes: Homecoming and may not reflect other City of Heroes server implementations.___

@Zed (Discord: Zed#7901)  
@Felis Noctu (Discord: Feles Noctis#9086)  
@Procat (Discord: Procat#3599)  
Metalios (Discord: Metalios#2673)

---

# Install Instructions
### Release Update
* Go to MRBU [Releases](https://github.com/zethriller/MRB-Updates/releases)
* Click __"Source code (zip)"__ under __"Assets"__ section of most recent Weekly
* Open downloaded file
* Extract contents of __"MRB-Updates-######"__ to Mids install folder, overwriting as prompted
  * _For a clean install, only extract the __"Data"__ and __"Images"__ folders_

### Cutting Edge
* Above right, find and click the green button labeled __"Clone or Download"__
* Click __"Download ZIP"__
* Open downloaded file
* Extract contents of __"MRB-Updates-master"__ to Mids install folder, overwriting as prompted
  * _For a clean install, only extract the __"Data"__ and __"Images"__ folders_

---

## __MRBU Features__
### Archetype Ordering
* MRBU currently orders the archetype selection dropdown menu in the same order as Homecoming's in-game list.
  * This does, however, cause the menu to have minimal organization other than by pre-Going Rogue factions, and may change in the future.  

### Database Version Number
* As of this Issue/Page number, the Mids database version is going to be formatted to match the year and matching Homecoming Issue/Page number of the last update, in order to make comparing versions at a glance easier for both devs and players.
  * __Year:__ 2020  
  __HC Vers:__ Issue 26, Page 4  
  __DB Date:__ 23/03/2020  
  __DB Vers:__ 20.2604

### Homecoming Beta Server Previews
* We’re in the process of adding Beta-specific content and changes to Mids’ to allow for analysis and number crunching of Homecoming’s beta changes. These sets may be found by looking for anything beginning with "zn_" (new) or "zc_" (changed), which in the case of powersets will push them to the bottom of their respective lists.
* As the beta server is changing much more frequently than on live, and the beta BIN files are currently difficult to parse to extract raw data, this added content may not always be 100% accurate. We’ll do our best to get them as close as we can!

---

## __To-Do__

### PAGE 5 SPECIFIC
* Polish pass of Electrical Melee
* Polish pass of Experimentation
* The following Scrapper and Stalker Epic Pools still need to be modified  
  _NOTE: These powersets were shared but now vary in values between Scrapper and Stalker, and so will need to be duplicated and made unique to each_
  * Leviathan Mastery
  * Mu Mastery
  * Soul Mastery
  * Weapon Mastery
* Dark Melee damage scales have not yet been applied as the value in Mids differs from the previous value reported in the HC patch notes. These sets will need to be reviewed in full.
* Dark Miasma/Darkness Affinity for Controller, Corruptor, Mastermind, and others were all mirroring Defender values for certain powers. This is true for Mids as well (Ranged_Ones provide raw values). These need to be changed to the appropriate AT-modifier categories and values reviewed for accuracy.

### General
* Snipe powers may be missing data
* Water Jet may be missing some data

### Power Updates & Fixes
* Scrapper > Titan Weapons > Defensive Sweep: Correct defense bonus to in-game value of 11.25%

### Incarnates
* One or more Lore pet sets appear to be missing (Demons primarily)

---

## __Known Issues__
### Need More Information
* Water Jet damage value for Blasters doesn’t match in-game.  
  _→ Will need to investigate calculation differences_

### Won’t Fix
* ATOs and Superior ATOs are not marked as mutually exclusive.  
  _→ Won't fix. Not related to database, and would require extensive Mids’ code changes to accomplish._
* Dominator > Martial Assault > Envenomed Blades isn't adding damage to other powers.  
  _→ Won't fix. The game's expression used to calculate added damage is complex and creates a damage bonus unique to each power based on the base power, recharge time, area factors if those exist, and some other calculations. Expressions are hardcoded into the database when the program is compiled, so we have no way of properly implementing this at this time. While we could go through and apply it to every power individually, that's excessive amounts of work for a relative edge case situation, and thus low priority._

---

# 2.6.0.7 I26P5 (2020-04-27)
_(20.2605)_

## __Client__
### Database Cleanup
* Deleted two unused, glitchy entries in Pets group
* All > Titan Weapon: Reorganized power redirects to more closely match their parents

### UI Fixes/Tweaks
* View Totals window has received some enhancements
  * Values have had their precision increased to 2 decimal places (#0.##) where appropriate to match in-game Totals
  * Misc Buffs > Movement > Fly: Calculations are now using BaseFlySpeed instead of MaxFlySpeed (oops!), and are now much closer to the actual in-game speeds  
    _→ KNOWN ISSUE: These values still do not quite match the in-game speeds due to calculation errors. This is, as far as we can tell, due to the use of negative offsets, which are necessary to properly implement enhancements but disagree with Mids' formulas. We're still working on this._  

## __Powers__
_→ KNOWN ISSUE FOR PAGE 5:_  
_We now have up to date raw data to work with, so expect a sweep across all powers to follow!_  
~~_We do not currently have the full power data and are working from the in-game tooltips, as well as using raw numbers instead of values affected by AT-modifiers. As such some numbers may not be 100% accurate at this time. This will be resolved as the raw data becomes available._~~

### New Support Powerset: Electrical Affinity
* Available for Controllers, Corruptors, Defenders, & Masterminds  
  _→ KNOWN ISSUE: Mids does not currently appear to be able to display Targeted Absorbs, so Insulating Circuit will show as (Self)._  

### New Origin Power Pool: Experimentation
* Available for all ATs

### New IO Sets
* Artillery (Targeted AoE, Rare, 30-50)
* Bombardment (Targeted AoE, Rare, 30-50)
* Preemptive Optimization (Endurance Modification, Uncommon, 21-50)
* Power Transfer (Endurance Modification, Rare, 21-50)
* Synapse’s Shock (Endurance Modification, Rare, 21-50)

### Power Updates & Fixes
* The following Scrapper and Stalker Epic Pools powers have been modified
  * Mace Mastery > Web Cocoon: This power now does Toxic Damage over time. Now accepts damage enhancements and sets.  
    _→ NOTE: Other epic sets to follow. Due to some scaling changes, these epic pools that Scrapper and Stalker previously shared are needing to be duplicated and made unique to each._
* All valid ATs > Invulnerability > Unstoppable: This power no longer accepts Endurance Mod enhancements or sets. The Recovery buff in this power has never been enhanceable
* Blaster > Epic > Mace Mastery: Power requirements updated to match in-game, descriptions updated to this functionality.  
  _→ NOTE: These requirements do not match the other epic sets. This has been reported to the Homecoming team._
  * Summon Spiderlings requires one power
  * Web Cocoon requires two powers
* Pool > Experimentation > Adrenal Booster: This power now accepts ToHit buff enhancements and IO sets.
* Stalker > Ice Melee > Ice Patch: This power no longer states that it accepts Universal Damage or Stalker Archetype Origin sets, it has never accepted these enhancements 

### Dark Melee
* All versions of Shadow Maul
  * Arc increased from 45 to 120 degrees
  * Recharge increased from 8 to 11 seconds 
  * Cast Time lowered from 3.07 to 2.35 seconds
  * Target Cap increased from 5 (10) to 10 (16) for Brutes, Scrappers, and Stalkers (and Tankers)  
    _→ TODO: Damage scales have not yet been applied as the value in Mids differs from the previous value reported in the HC patch notes. These sets will need to be reviewed in full._

### Dark Miasma
* All versions of Twilight Grasp
  * Accuracy increased from 1.0x to 1.2x  
    _→ TODO: Dark Miasma/Darkness Affinity for Controller, Corruptor, Mastermind, and others were all mirroring Defender values for certain powers. This is true for Mids as well (Ranged_Ones provide raw values). These need to be changed to the appropriate AT-modifier categories and values reviewed for accuracy._

### Pools
* The following Leadership powers have had their activation time reduced from 3.63 seconds to 1.5 seconds
  * Pools > Leadership > Maneuvers
  * Pools > Leadership > Assault
  * Pools > Leadership > Tactics
* Experimentation, Force of Will, and Sorcery are now mutually exclusive. In addition to a visual clue, there is a note about it in the powersets' descriptions.  
  _→ KNOWN ISSUE: Exclusivity is currently only shown when attempting to take powers from two sets._

### Enhancements & IOs
* Call of the Sandman: Chance for Heal
  * Heal increased from 5% to 15%
  * This proc is now unique

---

# 2.6.0.7 I26P4
_(20.2604)_  
_(Summary as of 2020-03-27)_

## __General Archetype Updates__
### Brute
* Fiery Aura powers updated to reflect current in-game values

### Corruptor
* Most primary specialization powers updated to reflect current in-game values
  * Does not include Snipe powers at this time
* Many Storm Summoning powers updated to reflect current in-game values

### Sentinel
* New icon for Beam Rifle primary set
* Reverted icon for Beam Rifle primary set, as this change was not introduced in-game

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
* Fixed Twilight Grasp "2 hits" healing on all support ATs
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
  * Arachnos Widow > Teamwork > Foresight resistance begins building at 75% Max HP, reaching 32.25% at 0% Max HP  
  _NOTE: Game description states it gives slope resistance to all damage types, but like SR's passives Foresight does not actually include Psionic or Toxic resistance._

### Pools
* Pools > Fighting > Cross Punch: Reordered power in set to avoid confusion
* Pools > Force of Will > Weaken Resolve: Reenabled slotting of Accurate ToHit Debuff enhancement sets as per in-game Manage Slots UI  
  → NOTE: If these IO sets cannot actually be slotted in-game, the Homecoming dev team should be informed.
* Sorcery and Force of Will are now mutually exclusive. In addition to a visual clue, there is a note about it in the powersets' descriptions  
  _→ KNOWN ISSUE: Exclusivity is only shown when attempting to take powers from two sets._

### Incarnates
* Enabling a Diamagnetic Interface will no longer debuff the player's regeneration, resistances, or tohit
* Enabling a Reactive Interface will no longer debuff the player's resistances

### IO Sets
* ATO > Might of the Tanker resistance proc no longer affected by Musculature Alpha
* ATO > Superior Might of the Tanker resistance proc no longer affected by Musculature Alpha
* Aegis: Psionic/Status Resistance effect text updated to reflect actual psionic resistance bonus
* Sudden Acceleration: Knockback to Knockdown 
  * This set will now only affect the power it is slotted in, as in-game.

## __Powers (HC beta)__
### New Support Powerset: Electrical Affinity
* __Label:__ zn_Electrical Affinity  
  _Up to date as of I26p5 Build 4_
  * Currently implemented for Controllers, Corruptors, Defenders, & Masterminds  
    _→ KNOWN ISSUE: Mids does not currently appear to be able to display Targeted Absorbs, so Insulating Circuit will show as (Self)._  
    _→ KNOWN ISSUE: We do not currently have the full power data and are working from the in-game tooltips, and are using raw numbers instead of values affected by AT-modifiers. As such the numbers may not be 100% accurate at all times. The Homecoming team has been contacted about the possiblility of getting their powers-related files directly._
  * Shock cast time has been increased to 12s from 8s
  * Chain distance has been added as radius
  * Mastermind: Defibrillate enhancements updated
    * Controllers, Corruptors, & Defender Defibrillate enhancements updated to mirror Mastermind

### New Origin Power Pool: Experimentation
* __Label:__ zn_Experimentation  
  _Up to date as of I26p5 Build 4_
* Added powerset icon
* Added scales and modifiers so it has variance among ATs
* Experimentation > Corrosive Vial:
  * Effects now use pseudo-pet

### Power Updates & Fixes
* The following Leadership _(zc_Leadership)_ powers have had their activation time reduced from 3.63 seconds to 1.5 seconds
  * Pools > Leadership > Maneuvers
  * Pools > Leadership > Assault
  * Pools > Leadership > Tactics

### Pools
* Experimentation, Sorcery, and Force of Will are now mutually exclusive. In addition to a visual
  clue, there is a note about it in the powersets' descriptions.  
  _→ KNOWN ISSUE: Exclusivity is only shown when attempting to take powers from two sets._

### IO Sets
* NEW
  * Artillery (Targeted AoE, Rare, 30-50)
  * Bombardment (Targeted AoE, Rare, 30-50)
  * Preemptive Optimization (Endurance Modification, Uncommon, 21-50)
  * Power Transfer (Endurance Modification, Rare, 21-50)
  * Synapse’s Shock (Endurance Modification, Rare, 21-50)
* Fixed the display of multiple procs/specials within the tooltip: Bombardment +FireDmg, Power Transfer +HealSelf, Synapse's Shock +RunSpeed.
* Power Transfer: Chance to Heal Self no longer marked as Unique
* Updated Artillery enhancements to match new icon
* Updated Bombardment icon
