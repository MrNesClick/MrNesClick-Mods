# Flux Networks Extended

![Flux Networks Extended](../assets/flux-networks-extended/logo.png){ align=right width="128" }

An addon for **[Flux Networks](https://www.curseforge.com/minecraft/mc-mods/flux-networks)**: higher tiers of Flux
Plugs and Flux Points, upgrade kits to raise a placed device to the next tier, and an optional Mekanism integration.

!!! warning "Beta"
    The features are complete and tested, but please back up your world before updating and
    [report what you find](https://github.com/MrNesClick/MrNesClick-Mods/issues/new/choose).

![An Ultimate Flux Plug and Point between two energy cubes, seen with The One Probe and Jade](../assets/flux-networks-extended/upgraded-ultimate.png)

## In short

- **Three new tiers**, named after Flux Networks' own Flux Storages: Herculean, Gargantuan and Ultimate Flux Plugs and
  Points. They join any Flux Network like the basic ones and take its colour.
- **Each tier has a ceiling.** The transfer limit of a device stops at its tier's max limit, *Bypass Limit* included.
- **Upgrade in place.** Right-click a placed Plug or Point with an upgrade kit: it becomes the next tier and keeps its
  network and every setting.
- **Mekanism (optional)**: the recipes use Mekanism's alloys and control circuits, and more than 2.1G FE/t goes through
  a single Plug and Point.
- **The One Probe and Jade (optional)** show the tier and max limit of the device you look at.
- **Configurable**: the limits of each tier, and an optional cap on Flux Networks' own Plugs and Points for servers that
  want the tiers to matter.

| Tier | Limit of a newly placed device | Max limit |
|---|---|---|
| Basic (Flux Networks) | 800,000 FE/t | unchanged, unless [capped](config.md#capping-the-basic-devices) |
| Herculean | 5,000,000 FE/t | 20,000,000 FE/t |
| Gargantuan | 50,000,000 FE/t | 200,000,000 FE/t |
| Ultimate | 1,000,000,000 FE/t | 10¹⁵ FE/t |

## Where to go next

- [Tiered Plugs and Points](devices.md): recipes, transfer limits, the device GUI, probes, wiping and breaking.
- [Upgrade kits](upgrade-kits.md): upgrading a placed device without breaking it.
- [Mekanism integration](mekanism.md): the Mekanism recipes and transfers above 2.1G FE/t.
- [Configuration](config.md): every option, with its default.

## Requirements

| Minecraft | Loader | Flux Networks | Optional |
|---|---|---|---|
| 1.21.1 | NeoForge 21.1.64+ | 8.x | Mekanism 10.7+, The One Probe, Jade |
| 1.20.1 | Forge 47+ | 7.2.1+ | Mekanism 10.4+, The One Probe, Jade |

This addon follows the versions maintained by Flux Networks: when Flux Networks updates, this addon updates too.

## Download

[CurseForge](https://www.curseforge.com/minecraft/mc-mods/flux-networks-extended) ·
[Report a bug](https://github.com/MrNesClick/MrNesClick-Mods/issues/new?template=1-flux-networks-extended-bug.yml)

Not affiliated with the Flux Networks or Mekanism authors.
