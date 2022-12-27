# Block

## Chance to Block

Base block chance is 18% for warrior and 10% for paladin.
You gain additional block chance from the mastery:

$$
Final\:Block\:Chance = Base\:Block\:Chance\:+\:Bonus\:Block\:Chance+\:Flat\:Modifiers
$$

$$
Bonus\:Block\:Chance = \frac{Mastery\:Bonus\times X}{Mastery\:Points \times X \times v + h}
$$

For Protection Paladin **X** is 1, for Protection Warrior **X** is 0.5

Flat modifiers such as [Holy Shield](https://www.wowhead.com/spell=152261/holy-shield){target=_blank} add to your block chance.


## Block Value
Blocking attacks causes them to deal reduced damage, this damage reduction is based on your block value.
Like armor this form of damage reduction (against physical damage) cannot exceed 85%.

$$
\frac{block\:value}{block\:value+k}
$$

## Spell Block
By default only attacks that deal physical damage can be blocked, some talents / abilities (eg. Holy Shield) allow spells to be blocked. The restriction on being able to block a spell is generally the same as for an attack, specifically you have to be facing the enemy and not be casting or channeling. The spell needs to be directed at you and deal impact damage (dots cannot be blocked this way).

See more [here](https://www.wowhead.com/news/blizzard-on-upcoming-protection-paladin-and-warrior-changes-in-dragonflight-holy-328776){target=_blank}

See **K Value** [Dragonflight](../system/constants-df.md), [Shadowlands](../system/constants-sl.md)
