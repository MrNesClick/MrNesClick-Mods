# Plugs et Points de tier

Les Flux Plugs et Points herculéens, gargantuesques et ultimes fonctionnent exactement comme ceux de Flux Networks : un
Plug fait entrer l'énergie dans le réseau, un Point la fait sortir. Ils se connectent à n'importe quel réseau Flux,
appareils de base et Flux Storages compris, et affichent la couleur du réseau. Ce qui change, c'est ce qu'ils peuvent
transférer par tick.

!!! note "Noms en anglais"
    Flux Networks n'est pas traduit en français : ses objets et les boutons de son interface (*Flux Plug*,
    *Flux Core*, *Power Surge*, *Bypass Limit*...) restent en anglais dans le jeu, et donc ici.

## Limites de transfert

| Tier | Limite d'un appareil posé | Limite max |
|---|---|---|
| Herculéen | 5 000 000 FE/t | 20 000 000 FE/t |
| Gargantuesque | 50 000 000 FE/t | 200 000 000 FE/t |
| Ultime | 1 000 000 000 FE/t | 10¹⁵ FE/t |

- Un appareil démarre à la limite par défaut de son tier. Réglez n'importe quelle valeur jusqu'à la limite max dans son
  interface.
- **Bypass Limit** ne dépasse pas le tier : un Flux Plug herculéen avec *Bypass Limit* activé transfère au plus
  20M FE/t.
- Les deux valeurs se règlent par tier dans la [config serveur](config.md). Les 10¹⁵ FE/t de l'ultime sont aussi la
  plus grande valeur acceptée par la config : voir [pourquoi](config.md#pourquoi-1015-fet-au-plus).

## Fabrication

Chaque tier se fabrique à partir du tier inférieur, placé au centre d'une table de craft (le Flux Plug ou Point de base
de Flux Networks pour le tier herculéen) :

| Résultat | Centre | 4 côtés | 4 coins |
|---|---|---|---|
| Flux Plug / Point herculéen | Flux Plug / Flux Point | Flux Core | Diamant |
| Flux Plug / Point gargantuesque | Flux Plug / Point herculéen | Flux Block | Lingot de netherite |
| Flux Plug / Point ultime | Flux Plug / Point gargantuesque | Herculean Flux Storage | Étoile du Nether |

L'appareil fabriqué garde le réseau de celui du centre (en Minecraft 1.21.1, ses réglages aussi), comme Flux Networks le
fait pour ses Flux Storages. Pour améliorer un appareil sans le ramasser, utilisez un
[kit d'amélioration](upgrade-kits.md).

!!! info "Avec Mekanism"
    Quand Mekanism est installé, ces recettes sont remplacées par des [recettes Mekanism](mekanism.md#recettes).

Tous les appareils et les kits sont dans leur propre onglet créatif, *Flux Networks Extended*, à côté de celui de Flux
Networks.

## L'interface de l'appareil

L'interface est celle de Flux Networks, avec quelques changements pour les grands nombres :

- Le champ de limite de transfert s'arrête à la limite max de l'appareil au lieu d'accepter n'importe quel nombre.
- Sur les appareils de tier, le champ s'appelle **Limite** au lieu de *Transfer Limit*, pour que les grandes valeurs
  restent lisibles.
- Les lignes de transfert et de tampon passent en format compact (10,0 GFE/t) quand le nombre complet déborderait du
  cadre.

![L'interface d'un Flux Plug ultime qui transfère 10G FE/t](../assets/flux-networks-extended/big-numbers-gui.png)

## The One Probe et Jade

Les deux sont optionnels. Regarder un Plug ou un Point de tier affiche son tier et sa limite max, par exemple
*Tier : Ultime (max 1 000 000 000 000 000 FE/t)*, sous les informations de Flux Networks. The One Probe affiche aussi
*Flux Networks Extended* comme nom de mod des appareils de tier, au lieu de *Flux Networks*.

Quand le [plafond des appareils de base](config.md#plafonner-les-appareils-de-base) est activé, les Plugs et Points de
Flux Networks l'affichent aussi : *Tier : De base (max 2 500 000 FE/t)*.

Dans Jade, la ligne peut être désactivée dans les réglages du plugin : *Tier des Flux Plugs et Points*.

L'infobulle d'un appareil ou d'un kit affiche le même tier et la même limite max.

## Démontage et effacement

- Un appareil cassé se ramasse avec son réseau et ses réglages, comme ceux de Flux Networks.
- Pour effacer les réglages d'un appareil, posez-le seul dans une grille de craft, comme pour les appareils de Flux
  Networks.
