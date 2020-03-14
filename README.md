# MRB-Updates
Unofficial Mids' Reborn updates

@Zed (Discord: Zed#7901)  
@Felis Noctu (Discord: Feles Noctis#9086)  
@Procat (Discord: Procat#3599)  
Metalios (Discord: Metalios#2673)

---

2.6.0.7b (WIP - 03/14/2020)  
* IO Sets  
  * Added Synapse's Shock, Power Transfer, Preemptive Optimization (EndMod), Bombardment, Artillery (RangedAOE). Up-to-date as of I26p5 build 3.
* Pools
  * Added Experimentation power pool, fixed powerset icon.  
  Note: values may be off, they differ depending on the AT.  
  Adjustments may be needed.
  * Sorcery, Force of Will and Experimentation are now mutually exclusive.  
  In addition to a visual clue, there is a note about it in the powersets' description.  
  KNOWN ISSUE: We are now aware that exclusivity is not complete and are returning to this.

* Brute/Scrapper/Sentinel/Stalker/Tanker
  * Implemented scaling values for Super Reflexes passives' damage resistance slope.  
  Note: Rounding errors may cause small inaccuracies at some values.  
  Note: Unlike most defensive numbers, these resistance slopes are not affected by AT modifiers. SR was originally only implemented on Scrappers and used hard values, and when it was proliferated to other ATs this didn't change.  
  Brute, Scrapper, and Tanker resistance begins building at 60% Max HP, reaching 20% res/passive at 0% Max HP.  
  Sentinel/Stalker resistance begins building at 60% Max HP, reaching 25% res/passive at 0% Max HP.

* Blaster
  * Atomic Manipulation > Beta Decay:  
  → Recharge bonus now correctly scales 10+0% at 0 stacks to 10+25% at 10 stacks.

* Defender
  * Added Electrical Affinity (formerly known as Shock Therapy), new primary powerset.  
  Note: Mids does not currently appear to be able to display Targeted Absorbs, so Insulating Circuit will show as (Self).

* Tanker
  * Updated secondary powersets' values (WIP)

* Widow
  * Implemented scaling values for Foresight's damage resistance slope.  
  Note: Rounding errors may cause small inaccuracies at some values.  
  Note: Paragon used the same formula as SR's passives but at a higher starting HP value. Game description states it gives slope resistance to all damage types, but like SR's passives does not actually include Psionic or Toxic resistance.  
  Foresight resistance begins building at 75% Max HP, reaching 32.25% at 0% Max HP.
  * Added scaling for Follow Up (1 to 4 stacks)


2.6.0.7a (01/14/2020)
* Corruptor
  * Adjusted all primary specs values, except for snipe powers (no info on these)
  * Adjusted damage and effects values for Storm Summonning
  * Beam Rifle.Lancer Shot: added missing DoT damage
  * Added missing DoT damage on entities: Whirlpool, Blizzard, Ice Storm, Freezing Rain, Rain of Fire. Tornado, Lightning Storm

* Stalker/Scrapper
  * Fix for Ancillary pool being locked when adding a snipe power. To do so, Quick Form has been moved to class' inherents and removed from ancillary pools - so it's always there even if you don't take any snipe power. This might unlock your existing builds (not tested)
		
* Blaster
  * Trick Arrow.EMP Arrow: adjusted endurance cost, updated description
  * Temporal Manipulation.Chronos: Mark power as a click-buff so it can have a green button toggle
  * Plant Manipulation.Wild Fortress: fixed absorb value

* Arachnos Widow
  * Fortunata & Night Widow: adjusted effect values for Mind Link

* Sentinel
  * Radiation Armor.Particle Shielding: allow slotting EndMod sets
  * Invulnerability.Durability: changed +Absorb effect to a +MaxHP one  
  Note: ingame effect is "max absorb", but is actually extra HitPoints. Therefore it will not be enhanced by Cardiac Radial Alpha.

* Brute
  * Fiery Aura (whole powerset): adjusted effect values.

* Pools
  * Force of Will.Weaken Resolve: power could receive Accurate ToHit Debuff sets, but not ingame.
  * Presence.Unrelenting: Mark power as a click-buff so it can have a green button toggle.
  * Flight.Hover: Adjusted endurance cost

* Incarnates
  * Enabling a reactive interface will not debuff player's resistances.  
  Also fixed for Diamagnetic interfaces althrough this one has no visible impact.


Known bugs/Todo
* All classes
  * Missing data on snipe powers and Water Jet


Misc - found in MRB discord
* ATOs and Superior ATOs are not marked as mutually exclusive.  
  → Won't fix. Would require extensive work to do so. 

* Water Jet dmg value for blasters in Mids vs In-game is off.  
  → I have no info about this power.

* Envenomed Blades in Dominators' Martial Assault secondary cannot be toggled on. There is no green button.  
  → Fixed.

* The defense of Titan Weapon's Defensive Sweep is incorrectly valued at 15% baseline in Mids' for a Scrapper, but in-game, it is 11.25%.  
  → Not modified, value is correct. Fixed in an older release ?

* Mids' not aggregating smash lethal resistance properly on fire brutes.  
  → Fixed.
