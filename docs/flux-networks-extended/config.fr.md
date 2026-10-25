# Configuration

Flux Networks Extended a un seul fichier de config, côté serveur et synchronisé avec les joueurs. Ses valeurs sont en FE
par tick.

## Fichier

| Minecraft | Emplacement |
|---|---|
| 1.21.1 (NeoForge) | `config/fluxnetworksextended-server.toml`. Pour un seul monde, copiez-le dans `<monde>/serverconfig/` et modifiez cette copie. |
| 1.20.1 (Forge) | `<monde>/serverconfig/fluxnetworksextended-server.toml`, créé avec chaque monde. Les modpacks mettent leurs valeurs par défaut dans `defaultconfigs/`. |

## Plafonner les appareils de base

Par défaut, les Plugs et Points de Flux Networks ne sont pas touchés : les réseaux existants fonctionnent comme avant.
Un serveur qui veut rendre les tiers nécessaires peut activer `capBasicDevices` : les appareils de base transfèrent
alors au plus `basicMaxLimit` (2 500 000 FE/t par défaut), *Bypass Limit* compris, et les débits plus élevés demandent
des appareils de tier.

- La limite enregistrée dans chaque appareil de base est conservée : désactiver le plafond la rétablit.
- Le champ de limite de leur interface s'arrête au plafond, et [The One Probe et Jade](devices.md#the-one-probe-et-jade)
  l'affichent.

![Un Flux Plug de base avec le plafond activé, vu avec The One Probe et Jade](../assets/flux-networks-extended/basic-cap.png)

## Pourquoi 10¹⁵ FE/t au plus

Toutes les limites de ce fichier, et la limite max de l'ultime, s'arrêtent à 10¹⁵ FE/t. Flux Networks additionne les
transferts d'un réseau sur 64 bits : des appareils sans limite sur des cubes d'énergie créatifs de Mekanism feraient
déborder ces sommes et arrêteraient tout le réseau
([signalé à Flux Networks](https://github.com/SonarSonic/Flux-Networks/issues/595)). 10¹⁵ FE/t laissent de la place
pour des milliers d'appareils à plein débit.

## Options

Le tableau reprend le fichier de config tel qu'il est écrit, donc en anglais, comme ses commentaires.

--8<-- "flux-networks-extended/server.md"
