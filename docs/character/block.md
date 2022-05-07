# Block

## Chance to Block

Block chance is primarily gained from the mastery of Protection Paladin and Protection Warrior.
The formula is the following.

$$
Final\:Block\:Chance = Base\:Block\:Chance\:+\:Bonus\:Block\:Chance+\:Flat\:Modifiers
$$

$$
Bonus\:Block\:Chance = \frac{Mastery\:Bonus\times X}{Mastery\:Points \times X \times v + h}
$$

Protection Paladin has **X** to be 1, while Protection Warrior has **X** to be 0.5

Your base block chance is always 10%. This is true for anyone who has the ability to block.

Flat modifiers are things such as [Holy Shield](https://www.wowhead.com/spell=152261/holy-shield), which increases your chance to block by 15%.


## Block Value
Blocking attacks causes them to deal reduced damage, this damage reduction is based on your block value.
This form of damage reduction is hard capped at 85%.

$$
\frac{block\:value}{block\:value+k}
$$

See [K Value](../system/constants-sl.md)