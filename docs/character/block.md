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

Flat modifiers are things such as [Holy Shield](https://www.wowhead.com/spell=152261/holy-shield){target=_blank} add to your block chance.


## Block Value
Blocking attacks causes them to deal reduced damage, this damage reduction is based on your block value.
This form of damage reduction is hard capped at 85%.

$$
\frac{block\:value}{block\:value+k}
$$

See **K Value** [Dragonflight](../system/constants-df.md), [Shadowlands](../system/constants-sl.md)