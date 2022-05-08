# Stat Scaling, Shadowlands values

## Portions of the budget allocated to items per slot per stat.

- Technically game tables specify the proportions per item (of which there are thousands), however with some exceptions where a stat is set to 0 the proportions for all are identical to below.
For example trinkets usually have one stat and the rest are zeroed.

| Slot | Primary | Secondary | Stamina |
| --- | --- | --- | --- |
| Armor / Weapons | 52.59% | 70% | 78.89% |
| Trinkets | 66.66% | 66.66% | 66.66% |
| Jewelry | 0% | 175% | 78.89% |

## Weights / Ratios, different gear slots have different weights for stats

- Chest pieces have more stats than Bracers, and although the game doesn't specify the weights explicitly each slot has it's own budget table, however the data in the tables is identical if you normalize for those weights.
- One handed wepons and shields are exactly one half of a two hander.

| Slot | Weight / Ratio |
| --- | --- |
| Chest, Pants, Helm, 2H Weapon | 1 |
| Shoulders / Belt / Boots / Gloves / Trinket | \(\frac{12}{16}\) |
| Bracers / Cloak / Jewelry | \(\frac{9}{16}\) |

## Armor types

- Here the game doesn't explicitly specify weights either but they are derivable from the armor budget.

| Type | Weight |
| --- | --- |
| Plate | 1 |
| Leather | 0.450825 |
| Cloth | \(\frac{89}{339} \approx 0.2625\) |

## Armor portions per slot

- Located in the `ArmorLocation` table (pun intended), these specify how much of the 'total' each slot is allocated.
- Shields are not strictly in that table, however those have their own budget function which is proportional to the general function.

| Slot | Weight / Ratio | Normalized weight |
| --- | --- | --- |
| Chest | 0.16 | 1 |
| Pants | 0.14 | \(\frac{14}{16}\) |
| Helm | 0.12 | \(\frac{12}{16}\) |
| Shoulders / Cloak | 0.11 | \(\frac{11}{16}\) |
| Boots | 0.10 | \(\frac{10}{16}\) |
| Belt / Gloves | 0.09 | \(\frac{9}{16}\) |
| Bracers | 0.08 | \(\frac{8}{16}\) |
| Shield | \(\approx 0.46881584 \) | \(\approx 2.93\) |