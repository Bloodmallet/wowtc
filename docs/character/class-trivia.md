## Paladin

### Holy Shield

Despite the description does not allow you to **block** spells, it grants you the ability to absorb spells, it does not require a shield to activate or face the target or in fact even have a target.

It's an absorb that has a chance equal to you block chance to proc and it's value is based on the block value of your shield.

For example not having a shield equipped will still proc Holy Shield that doesn't absorb anything (since your block value is 0) but deals damage if the damage that was 'absorbed' is sourced to a valid target.

From the above the two effects (absorb and damage) can both happen or only one can, though damaging a target and not absorbing is fairly unlikely unless you for some reason chose to not use a shield.

### Blessed Hammer

Rotates clockwise in an [Archimedean spiral](https://www.desmos.com/calculator/gfmndxsmek){target=_blank} starting directly behind you (3/2pi) and finishing 2 rotations after 5 seconds at the same angle reaching roughly 10y range at the final point.

It can hit the same target anywhere from 0 to N times depending on the size of target's hit box, presumably every time it intersects the hit box (usually ~2 hits on normal sized mobs).

The debuff it applies 'works' on **any** damage as long as it's sourced to the target with the debuff.


## Monk

### Stagger

Uppon exiting combat your stagger pool is removed after at most 4 seconds (8 ticks).

### Black Ox Statue

Pulses threat in a radius (?y) every 3s, the amount of threat per pulse is x1.25 of your total AP

Has 50% of your HP at the time of summon, ~95% damage reduction against AoE, ~15% damage reduction against direct magic damage, ~75% damage reduction against direct physical damage.


## Shaman

### Mastery: Elemental Overload
Elemental Overloads happen after a delay of 0.4 seconds after the player spell was cast successfully.
Elemental Overload spells are separate spells to the ones the player is casting.
The spell [Mastery: Elemental Overload](https://www.wowhead.com/spell=168534/mastery-elemental-overload) mentions Overloads to have a strength of 85% (PvP: 75%) of the base spells.
Each Overload spelldata matches the spellpower coefficient of the base spell. The aforementioned multiplier is applied to that.

!!! warning ""
    Because player spells and Overloads are separate spells there occasionally existed times when Overloads did not deal an appropriate amount of damage. 

| Player spell | Elemental Overload spell | Type |
| --- | --- | --- |
| [Chain Lightning](https://www.wowhead.com/spell=188443/chain-lightning) | [Chain Lightning Overload](https://www.wowhead.com/spell=45297/chain-lightning-overload) | Baseline |
| [Lightning Bolt](https://www.wowhead.com/spell=188196/lightning-bolt) | [Lightning Bolt Overload](https://www.wowhead.com/spell=45284/lightning-bolt-overload) | Baseline |
| [Lava Burst](https://www.wowhead.com/spell=285452/lava-burst) | [Lava Burst Overload](https://www.wowhead.com/spell=285466/lava-burst-overload) | Baseline |
| [Elemental Blast](https://www.wowhead.com/spell=117014/elemental-blast) | [Elemental Blast Overload](https://www.wowhead.com/spell=120588/elemental-blast-overload) | Talent |
| [Icefury](https://www.wowhead.com/spell=210714/icefury) | [Icefury Overload](https://www.wowhead.com/spell=219271/icefury-overload) | Talent |

!!! info ""
    There are even more spells with the above names.
    Each with a different sub-set of data associated.
    At the time of writing it is not known why these exist or which one is actually the "primary" spell.

!!! warning "[Chain Lightning](https://www.wowhead.com/spell=188443/chain-lightning)"
    Spell rolls its Overload chance on each target hit.
    Overload chance is 1/3 of the actual percentage shown in [Mastery: Elemental Overload](https://www.wowhead.com/spell=168534/mastery-elemental-overload).
    [Chain Lightning Overload](https://www.wowhead.com/spell=45297/chain-lightning-overload) tries to chain to as many nearby targets as [Chain Lightning](https://www.wowhead.com/spell=188443/chain-lightning) can.

### Maelstrom
Some spells generate Maelstrom.
Which spells are and how much is stored in "[Maelstrom](https://www.wowhead.com/spell=343725/maelstrom)".
Each effect of this spell describes a Maelstrom amount of a spell.
The tooltip of this spell does not show all effects.

### Surge of Power
The talent [Surge of Power](https://www.wowhead.com/spell=262303/surge-of-power) adds additional Overloads to the next [Lightning Bolt](https://www.wowhead.com/spell=188196/lightning-bolt).
These additional Overloads have an additional time delay compared to baseline Overloads.

| Additional Overload Count | Chance |
| --- | --- |
| 3 | 2% |
| 2 | 18% |
| 1 | 80% |

An alternative approach is to assume 1 additional Overload to be the starting point of this talent.
This starting point has a 20% chance to upgrade itself to at least 2 Overloads.
These 2 Overloads again have a 20% chance to upgrade themselves to 3 Overloads. 

!!! info "How to reproduce"
    1. Cast [Lightning Bolt](https://www.wowhead.com/spell=188196/lightning-bolt) and [Earth Shock](https://www.wowhead.com/spell=8042/earth-shock) at a target dummy. 
    1. Filter the log to [Lightning Bolt](https://www.wowhead.com/spell=188196/lightning-bolt) and their Overloads right after casting [Earth Shock](https://www.wowhead.com/spell=8042/earth-shock).
    1. Remove baseline Overloads.
