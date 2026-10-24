# Upgrades

The wellhead takes Mekanism's **Speed** and **Energy** upgrades, up to 8 of each, in Mekanism's upgrade tab or with a
sneak + right-click on the wellhead. As on Mekanism's machines, a multiplier M applies as M^(n/8) with n upgrades.

![Mekanism's upgrade window on a wellhead](../assets/mekanistic-geothermal/media-07-upgrades.png)

## Speed

- **Drilling**: ×10 faster with 8 upgrades (4 ticks per block instead of 40).
- **Steam**: the max steam rate doubles with 8 upgrades (800 mB/t for the Basic tier). The water use follows.
- **The price, as in Mekanism**: the energy per tick grows with the square of the speed. Drilling energy per tick
  ×100 with 8 upgrades (the same energy per block, ten times faster), control system ×4. The extra steam also counts in
  the [exhaustion](wellhead.md#exhaustion) load: twice the steam, twice the wear.

## Energy

- Drilling and control system energy ÷10 with 8 upgrades.
- Energy buffer ×10 (4,000,000 FE for the Basic tier).

## With both

8 Speed and 8 Energy: 4 ticks and 4,000 FE per block, 800 mB/t of steam, 8 FE/t for the control system.

Every multiplier, and whether Speed affects steam and the control system, is in the
[`[upgrades]` section](config.md#upgrades) of the config.
