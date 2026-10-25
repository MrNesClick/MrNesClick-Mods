# Mekanism integration

Mekanism is optional. When it is installed, two things change.

## Recipes

The tier recipes, for devices and upgrade kits alike, use Mekanism's alloys and control circuits instead of the
standard materials. The standard recipes are not loaded then.

| Tier | 4 sides | 4 corners |
|---|---|---|
| Herculean | Infused Alloy | Advanced Control Circuit |
| Gargantuan | Reinforced Alloy | Elite Control Circuit |
| Ultimate | Atomic Alloy | Ultimate Control Circuit |

As without Mekanism, a device recipe has the tier below in the centre, and a kit recipe leaves the centre empty. See
[crafting](devices.md#crafting) and [upgrade kits](upgrade-kits.md#recipes).

## Transfers above 2.1G FE/t

Forge Energy counts in 32-bit numbers, so one block can pass at most 2,147,483,647 FE per tick through it. Tiered
Plugs and Points talk to Mekanism through Flux Networks' long energy API instead: a single Plug and a single Point can
move more than that between Mekanism blocks. 10G FE/t through one Plug and one Point is checked in the mod's tests.

Blocks of mods that do not support this API still go through Forge Energy, with its 2.1G FE/t limit per block.
