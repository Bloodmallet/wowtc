# Threat

## General description

Each monster has a threat table, it sums all the 'hostile' actions performed against it per actor (player, pet etc.). These actions are damage, healing and generating rage (and only rage).

Actors are generally separate entities, so a player's pet/totem/minion generates threat for itself, with some exceptions, eg. Dancing Rune weapon (it's hypothesized that the distinction is when said actor is never targetable).

Generally within end game content threat is 1 to 1 with damage (in open world or content where level scaling is applied that may vary) and healing is 1 to 0.5 split among all enemies in combat.

Druids in bear form and protection warriors gain threat from generating rage, though it seems archaic (a vestige from classic), the threat is split between all enemies in combat (the amount of threat generated this way is negligble).

## Target selection

A monster chooses to attack an eligible actor with preference to it's melee range. It chooses a new target if said target exceedes **110%** threshhold of the current target's threat if the new target is in melee range and **130%** if it is not.

Some actions may force a target selection, eg. if the current target becomes in-eligible (Immune), 'dropping' threat, taunting.

## Taunt

- Forces the target to attack you for a duration
- Increases your threat against the target to the value of whoever is tanking (if whoever is tanking has more threat than you, also see **1,2**)
- Applies a debuff to the target for a duration that increases threat conversion by **400%** (x5)

**1**. Your cotank is the current target but has less threat than a mage who is at 125% threat, taunting will make you the target but you will have less threat than the mage.

**2**. Your cotank is about to overagro, taunting will not equalize your threat, it will only apply the taunt debuff to the monster.

Most bosses gain 'resistance' to taunt's effects when they are taunted repeatedly, generally referred to as taunt 'dr'. Bosses whose mechanics necessitate frequent taunts are exempt on a case by case basis.

Specifically each taunt's duration after the first is reduced by **35%** successively up to 5 times eg. [3s, 1.95s, ~1.27s, ~0.82s, 0.53s, immune].

That resistance/'dr' is reset after **20s** of the boss not being taunted or being immune.

## Tanks

- Tank specs/forms have a modifier that increases threat conversion by **450%** (you generate x5.5 damage as threat)
- Some spells when executed by a tank have an additional modifier to threat, see the table (the location for that modifier is unknown)
- Dancing Rune Weapon generates x10 threat from damage that's attributed to the player
- Tank specs/forms are *supposed* to not generate threat from healing, this is implemented via blacklisting in the spec's 'aura' and on specific spells (*there are exceptions*).

	Since the effects need to be manually blacklisted expect plenty of exceptions, some notables in Shadowlands are Indomitable, Condensed Anima Sphere and Keg of Heavens, there are very likely others.
- All threat modifiers are multiplicative, eg. *a Protection Warrior casts Taunt followed by Heroic Throw on a target:

	Heroic Throw deals 100 damage* and generates `100*5.5*5*4=11000` threat (x5.5 from protection spec, x5 from Taunt debuff, x4 from Heroic Throw modifier).

### 'Special' spells

| Spell | Modifier |
| --- | --- |
| Throw Glaive | +300% (x4) |
| Heroic Throw | +300% (x4) |
| Thrash (dot) | +100% (x2) |

### Threat Modifiers

| Spec | 450% increased threat | No threat from healing |
| --- | --- | --- |
| Vengence | Increased Threat (id=189926) | specific spells via `No Threat (42)` flag |
| Druid | Bear Form Passive 2 (id=21178) | (id=299393) [Rejuvenation, Cenarion Ward, Renewal], specific spells via `No Threat (42)` flag |
| Blood | Aura, #9 (id=260810) | (id=40418, 805637) [Death Coil, Unholy Strength], specific spells via `No Threat (42)` flag |
| Brew | Aura, #12 (id=260843) | (id=739778) [Chi Wave, Chi Burst], specific spells via `No Threat (42)` flag |
| Prot. Warrior | Aura, #4 (id=191018) | (id=261030) [Victory Rush], specific spells via `No Threat (42)` flag |
| Prot. Paladin | Righteous Fury (id=25780) | (id=256092) [Lay on Hands, Flash of Light, Word of Glory, Arcing Light], specific spells via `No Threat (42)` flag |