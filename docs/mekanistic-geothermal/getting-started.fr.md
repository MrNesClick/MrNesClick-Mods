# Prise en main

D'une tête de puits neuve à la vapeur dans une turbine Mekanism. Le **Guide** de la tête de puits (l'onglet **?** de
son interface) reprend les mêmes étapes, et s'ouvre de lui-même tant que le puits n'a pas encore produit de vapeur.

![Le guide d'une tête de puits neuve](../assets/mekanistic-geothermal/media-04-guide.png)

## 1. Fabriquer

| Objet | Recette |
|---|---|
| **Tubage de puits en acier** ×8 | 4 lingots d'acier en losange : `_S_` / `S_S` / `_S_` |
| **Tête de puits géothermique basique** | `SCS` / `AMA` / `SDS` : S lingot d'acier, C circuit de contrôle de base, A alliage infusé, M boîtier en acier de Mekanism, D diamant |
| **Adaptateur logique géothermique** (optionnel) | `SRS` / `RCR` / `SQS` : S lingot d'acier, R redstone, C circuit de contrôle de base, Q comparateur |

Les recettes utilisent des tags communs (`c:ingots/steel`, `c:circuits/basic`, `mekanism:alloys/infused`...) : l'acier
et les circuits d'autres mods fonctionnent aussi, et un datapack peut les remplacer.

La colonne prend **un tubage par bloc foré** : une tête de puits au niveau de la mer (Y 63) forée jusqu'à Y −60 demande
environ 124 tubages, soit 62 lingots d'acier.

## 2. Poser et alimenter

Posez la tête de puits là où vous voulez le puits : elle fore tout droit, sous elle. Laissez **de l'air au-dessus** : la
face du haut est la soupape de sécurité.

Par défaut, **toutes les faces sauf celle du haut** acceptent l'énergie, l'eau et les tubages, et sortent la vapeur et
les déblais. La vapeur est éjectée automatiquement, les déblais non. Changez-le dans l'onglet de configuration des faces
de Mekanism, ou avec un Configurateur, comme pour n'importe quelle machine Mekanism.

Branchez l'**énergie** (câble universel ou toute source de FE) : le forage coûte 4 000 FE par bloc, et le système de
contrôle 20 FE/t une fois la colonne en place. La réserve contient 400 000 FE.

## 3. Tubages et forage

1. Mettez des **tubages de puits en acier** dans les emplacements de tubage (4 emplacements de 64), ou amenez-les par
   un tuyau ou un entonnoir.
2. Réglez la **profondeur cible** avec les flèches à côté de la valeur Y (Maj : ±10, ou la molette). La cible est un Y
   absolu ; l'écran affiche les blocs restants et les tubages nécessaires.
3. Appuyez sur **Démarrer le forage**. La foreuse descend d'un bloc toutes les 2 secondes, prend un tubage par bloc,
   range ce qu'elle creuse dans les emplacements de déblais, et s'arrête à la cible ou quand elle rencontre de la lave.

Changer la cible arrête le forage jusqu'à ce que vous appuyiez à nouveau sur le bouton. Une colonne endommagée est
réparée automatiquement, sans le bouton.

## 4. L'eau

Amenez de l'**eau** par un tuyau (pompe électrique de Mekanism, ou toute source d'eau qui pousse du fluide). Un puits
consomme un peu plus d'eau que la vapeur qu'il produit : 5 % sont perdus en purge.

## 5. La chaleur

La vapeur demande de la chaleur, et la chaleur dépend de **la profondeur du fond du puits**. Dans l'Overworld, la
température est de 100 °C à Y 0 et au-dessus (pas de vapeur : l'eau ne bout qu'au-delà) et monte jusqu'à **250 °C à
Y −60**, où le puits produit ses **400 mB/t** complets. La lave à 2 blocs ou moins du fond ajoute 2 °C par bloc de
source, jusqu'à 50 °C : elle aide un puits moins profond à atteindre son plein débit (le débit lui-même reste plafonné
à celui du tier par défaut).

| Fond du puits | Température | Vapeur (basique, sans amélioration) |
|---|---|---|
| Y 0 et au-dessus | 100 °C | aucune |
| Y −30 | 175 °C | 200 mB/t |
| Y −60 et en dessous | 250 °C | 400 mB/t |

Le Nether est à 180 °C à toute profondeur mais produit moins (×0,6) ; l'End n'a pas de chaleur exploitable.

## 6. La sortie de vapeur

Branchez un **tube pressurisé** vers une **turbine industrielle** de Mekanism (Mekanism Generators), un réservoir
chimique ou toute machine qui accepte la vapeur de Mekanism. La vapeur est éjectée automatiquement par toutes les faces
sauf celle du haut.

Si la vapeur n'a nulle part où aller, la pression monte : la soupape évacue au-dessus de 80 % et le système de contrôle
arrête la production à 90 %. Voir [Sécurité](safety.md).

![L'écran principal de la tête de puits](../assets/mekanistic-geothermal/media-03-interface.png)
