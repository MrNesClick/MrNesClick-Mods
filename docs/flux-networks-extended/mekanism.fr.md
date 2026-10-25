# Intégration Mekanism

Mekanism est optionnel. Quand il est installé, deux choses changent.

## Recettes

Les recettes des tiers, pour les appareils comme pour les kits d'amélioration, utilisent les alliages et les circuits
de contrôle de Mekanism à la place des matériaux standard. Les recettes standard ne sont alors pas chargées.

| Tier | 4 côtés | 4 coins |
|---|---|---|
| Herculéen | Alliage infusé | Circuit de contrôle avancé |
| Gargantuesque | Alliage renforcé | Circuit de contrôle d'élite |
| Ultime | Alliage atomique | Circuit de contrôle ultime |

Comme sans Mekanism, la recette d'un appareil a le tier inférieur au centre, et celle d'un kit laisse le centre vide.
Voir la [fabrication](devices.md#fabrication) et les [kits d'amélioration](upgrade-kits.md#recettes).

## Transferts au-delà de 2,1G FE/t

Forge Energy compte sur 32 bits : un bloc peut faire passer au plus 2 147 483 647 FE par tick. Les Plugs et Points de
tier échangent avec Mekanism par l'API d'énergie long de Flux Networks à la place : un seul Plug et un seul Point
peuvent transférer davantage entre des blocs Mekanism. 10G FE/t par un Plug et un Point sont vérifiés dans les tests
du mod.

Les blocs des mods qui ne prennent pas en charge cette API passent toujours par Forge Energy, avec sa limite de
2,1G FE/t par bloc.
