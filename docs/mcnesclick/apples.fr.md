# Pommes

Trois nouvelles pommes, et votre mot à dire sur la fréquence des pommes sur les feuilles.

## Pomme cuite

Faites cuire une pomme ordinaire pour obtenir une **Pomme cuite**. Elle rend **8 points de faim (4 pilons)** et
**12 de saturation**, bien plus qu'une pomme crue (4 de faim, 2,4 de saturation).

| Bloc | Temps | XP | Activée par défaut |
|---|---|---|---|
| Four | 10 s | 0,35 | oui |
| Fumoir | 5 s | 0,35 | oui |
| Feu de camp | 30 s | 0,35 | oui |
| Haut fourneau | 5 s | 0,35 | non : le haut fourneau vanilla ne cuit jamais de nourriture |

La pomme cuite est dans l'onglet créatif *Nourriture et boissons* (*Nourriture* avant Minecraft 1.19.3).

![Des pommes qui cuisent dans un four, un fumoir et sur un feu de camp](../assets/mcnesclick/cooked-apple-kitchen.png)

**Configurable** dans [`[cooked_apple]`](config.md#cooked_apple) : chaque mode de cuisson, la faim et la saturation.

## Pommes d'émeraude et de diamant

Deux pommes fabriquées l'une à partir de l'autre, avec des effets utiles plutôt qu'une pomme dorée plus forte. Les deux
se mangent toujours, même avec la barre de faim pleine, et rendent 4 de faim et 9,6 de saturation comme une pomme dorée.

| Pomme | Recette (table de craft) | Effets |
|---|---|---|
| **Pomme d'émeraude** | une pomme dorée entourée de 8 émeraudes | Héros du village et Chance, 5 minutes : à manger avant une séance de commerce |
| **Pomme de diamant** | une pomme d'émeraude avec 4 diamants sur les côtés et 4 éclats d'améthyste dans les coins | Célérité II et Vision nocturne, 5 minutes : à manger avant une expédition à la mine |

```
Pomme d'émeraude       Pomme de diamant
E E E                  A D A
E G E                  D M D
E E E                  A D A

E = émeraude, G = pomme dorée, A = éclat d'améthyste, D = diamant, M = pomme d'émeraude
```

![Les pommes dorée, d'émeraude et de diamant](../assets/mcnesclick/gem-apples.png)

![Les recettes des pommes d'émeraude et de diamant](../assets/mcnesclick/gem-recipes.png)

**Configurable** dans [`[emerald_apple]`](config.md#emerald_apple) et [`[diamond_apple]`](config.md#diamond_apple) :
la recette, la faim, la saturation et la liste des effets. N'importe quel effet fonctionne, y compris ceux des mods.

## Pommes des feuilles

En vanilla, seules les feuilles de chêne et de chêne noir donnent des pommes, 0,5 % du temps. MCNesclick garde ce
comportement par défaut, et vous permet :

- de changer la chance pour les feuilles de chêne et de chêne noir,
- de laisser toutes les autres feuilles donner des pommes aussi (bouleau, épicéa, acajou, acacia, cerisier, palétuvier,
  azalée, feuilles de mods…), avec leur propre chance (0,25 % une fois activées).

Comme en vanilla, les feuilles cassées aux cisailles ou avec Toucher de soie ne donnent pas de pommes, et les feuilles
qui se décomposent en donnent aussi. Fortune augmente toujours la chance sur les feuilles de chêne et de chêne noir.

![Des pommes qui tombent de différentes sortes de feuilles](../assets/mcnesclick/apples-from-leaves.png)

**Configurable** dans [`[apple_drops]`](config.md#apple_drops).
