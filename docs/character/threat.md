# Threat

## General description

Each monster has a threat table, it sums all the 'hostile' actions performed against it per actor (player, pet etc.). These actions are damage, healing and generating rage (and only rage).

Actors are generally separate entities, so a player's pet/totem/minion generates threat for itself with some exceptions, eg. Dancing Rune weapon (it's hypothesized that the distinction is when said actor is never targetable).

Generally within end game content threat is 1 to 1 with damage (in open world or content where level scaling is applied that may vary) and healing is 1 to 0.5 split among all enemies in combat.

Druids in bear form and protection warriors gain threat from generating rage, though it seems archaic (a vestige from classic), the threat is split between all enemies in combat, the amount of threat generated this way is negligble.

## Target selection

A monster chooses to attack an eligible actor with preference to it's melee range. It chooses a new target if said target exceedes **110%** threshhold of the current target's threat when the new target is in melee range and **130%** if it is not.

Some actions may force a target selection, eg. if the current target becomes in-eligible (Immune), 'dropping' threat, taunting.

## Tanks

- Tank specs/forms have a modifier that increases threat conversion by **450%** (you generate x5.5 damage as threat)
- Throw Glaive and Heroic Throw gain additional **300%** threat (x4) when executed by a tank spec
- Tank specs/forms generally do not generate threat from healing, some of it is defined in that spec's 'aura' and some on specific spells (*there are exceptions*). Some notable exceptions in Shadowlands are Indomitable and Condensed Anima Sphere, there are likely others.

All threat modifiers are multiplicative, eg. *a Protection Warrior casts Taunt followed by Heroic Throw on a target:
Heroic Throw deals 100 damage* and generates `100*5.5*5*4=11000` threat (x5.5 from protection spec, x5 from Taunt debuff, x4 from Heroic Throw modifier).

## Taunt

- Forces the target to attack you for a duration
- Sets your threat against the target to the highest value currently on the monster's threat table
- Applies a debuff to the target for a duration that increases threat conversion by **400%** (x5)

Most bosses gain 'resistance' to taunt's effects when they are taunted repeatedly, generally referred to as taunt 'dr'. Bosses whose mechanics necessitate frequent taunts are exempt on a case by case basis.

Specifically each taunt's duration after the first is reduced by **35%** successively up to 5 times eg. [3s, 1.95s, ~1.27s, ~0.82s, 0.53s, immune].

That resistance/'dr' is reset after **20s** of the boss not being taunted or being immune.

### TODO

- Check whether taunt actually set your threat to the highest value in the table rather than the value of the target currently tanking, the distinction being that you can be the current target and not be the highest on the table
- Add specific locations where threat modifiers may be found in the data